<script lang="ts">
  export let size: string = '15';
  export let role: string = 'img';
  export let color: string = 'black';
  export let variation: 'solid' | 'outline' = 'outline';
  export let ariaLabel = 'border radius';
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
      d="M10 1.5H11M13 1.5H14M13 4.5H14M13 7.5H14M13 10.5H14M13 13.5H14M10 13.5H11M7 13.5H8M4 13.5H5M1 13.5H2M1 10.5H2M1.5 8V5.5C1.5 3.29086 3.29086 1.5 5.5 1.5H8"
      stroke={color}
    />
  {:else}
    <path
      fill-rule="evenodd"
      clip-rule="evenodd"
      d="M5.5 2C3.567 2 2 3.567 2 5.5V8H1V5.5C1 3.01472 3.01472 1 5.5 1H8V2H5.5ZM11 2H10V1H11V2ZM14 2H13V1H14V2ZM14 5H13V4H14V5ZM14 8H13V7H14V8ZM2 11H1V10H2V11ZM14 11H13V10H14V11ZM2 14H1V13H2V14ZM5 14H4V13H5V14ZM8 14H7V13H8V14ZM11 14H10V13H11V14ZM14 14H13V13H14V14Z"
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
