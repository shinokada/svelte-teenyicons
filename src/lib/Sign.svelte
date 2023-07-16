<script lang="ts">
  export let size: string = '15';
  export let role: string = 'img';
  export let color: string = 'currentColor';
  export let variation: 'solid' | 'outline' = 'outline';
  export let ariaLabel = 'sign';
</script>

<svg
  xmlns="http://www.w3.org/2000/svg"
  width={size}
  height={size}
  fill="none"
  {...$$restProps}
  {role}
  aria-label={ariaLabel}
  viewBox="0 0 15 15"
  on:click
  on:mouseenter
  on:mouseleave
  on:mouseover
  on:mouseout
  on:blur
  on:focus
>
  {#if variation === 'outline'}
    <path
      d="M4.5 6.5V6C4.22386 6 4 6.22386 4 6.5H4.5ZM14.5 6.5H15C15 6.22386 14.7761 6 14.5 6V6.5ZM14.5 12.5V13C14.7761 13 15 12.7761 15 12.5H14.5ZM4.5 12.5H4C4 12.7761 4.22386 13 4.5 13V12.5ZM1 1V15H2V1H1ZM0 4H15V3H0V4ZM4.5 7H14.5V6H4.5V7ZM14 6.5V12.5H15V6.5H14ZM14.5 12H4.5V13H14.5V12ZM5 12.5V6.5H4V12.5H5ZM6 3.5V6.5H7V3.5H6ZM12 3.5V6.5H13V3.5H12Z"
      fill={color}
    />
  {:else}
    <path
      fill-rule="evenodd"
      clip-rule="evenodd"
      d="M1 1V3H0V4H1V15H2V4H6V6H4.5C4.22386 6 4 6.22386 4 6.5V12.5C4 12.7761 4.22386 13 4.5 13H14.5C14.7761 13 15 12.7761 15 12.5V6.5C15 6.22386 14.7761 6 14.5 6H13V4H15V3H2V1H1ZM7 6V4H12V6H7Z"
      fill={color}
    />
  {/if}
</svg>

<!--
  @component
  [Go to Document](https://svelte-teenyicons.codewithshin.com/)

  ## Props
  @prop size: string = "15";
  @prop role: string = "icon file name";
  @prop color: string = "black" 
  @prop variation: "solid" | "outline" = "outline";
  @prop ariaLabel = 'icon file name';
  ## Event
  - on:click 
  - on:mouseenter 
  - on:mouseleave 
  - on:mouseover 
  - on:mouseout 
  - on:blur 
  - on:focus 
-->
