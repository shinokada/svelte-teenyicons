<script lang="ts">
  export let size: string = '15';
  export let role: string = 'img';
  export let color: string = 'black';
  export let variation: 'solid' | 'outline' = 'outline';
  export let ariaLabel = 'lock small';
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
      d="M5.5 7H9.5V6H5.5V7ZM10 7.5V10.5H11V7.5H10ZM9.5 11H5.5V12H9.5V11ZM5 10.5V7.5H4V10.5H5ZM5.5 11C5.22386 11 5 10.7761 5 10.5H4C4 11.3284 4.67157 12 5.5 12V11ZM10 10.5C10 10.7761 9.77614 11 9.5 11V12C10.3284 12 11 11.3284 11 10.5H10ZM9.5 7C9.77614 7 10 7.22386 10 7.5H11C11 6.67157 10.3284 6 9.5 6V7ZM5.5 6C4.67157 6 4 6.67157 4 7.5H5C5 7.22386 5.22386 7 5.5 7V6ZM6 6.5V5.5H5V6.5H6ZM9 5.5V6.5H10V5.5H9ZM7.5 4C8.32843 4 9 4.67157 9 5.5H10C10 4.11929 8.88071 3 7.5 3V4ZM6 5.5C6 4.67157 6.67157 4 7.5 4V3C6.11929 3 5 4.11929 5 5.5H6Z"
      fill={color}
    />
  {:else}
    <path
      fill-rule="evenodd"
      clip-rule="evenodd"
      d="M10 5.5V6.08535C10.5826 6.29127 11 6.84689 11 7.5V10.5C11 11.3284 10.3284 12 9.5 12H5.5C4.67157 12 4 11.3284 4 10.5V7.5C4 6.84689 4.4174 6.29127 5 6.08535V5.5C5 4.11929 6.11929 3 7.5 3C8.88071 3 10 4.11929 10 5.5ZM6 5.5C6 4.67157 6.67157 4 7.5 4C8.32843 4 9 4.67157 9 5.5V6H6V5.5Z"
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
