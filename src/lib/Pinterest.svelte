<script lang="ts">
  export let size: string = '15';
  export let color: string = 'black';
  export let variation: 'solid' | 'outline' = 'outline';
  export let ariaLabel = 'pinterest';
</script>

<svg
  xmlns="http://www.w3.org/2000/svg"
  width={size}
  height={size}
  fill="none"
  class={$$props.class}
  {...$$restProps}
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
      d="M4.5 13.5L7.5 6.5M4.26389 9.5C3.78885 8.96924 3.5 8.26835 3.5 7.5V7C3.5 5.067 5.067 3.5 7 3.5H8C9.933 3.5 11.5 5.067 11.5 7V7.5C11.5 9.15685 10.1569 10.5 8.5 10.5C7.60421 10.5 6.80893 9.92679 6.52566 9.07697L6.5 9M7.5 14.5C3.63401 14.5 0.5 11.366 0.5 7.5C0.5 3.63401 3.63401 0.5 7.5 0.5C11.366 0.5 14.5 3.63401 14.5 7.5C14.5 11.366 11.366 14.5 7.5 14.5Z"
      stroke={color}
    />
  {:else}
    <path
      d="M0 7.5C0 3.35786 3.35786 0 7.5 0C11.6421 0 15 3.35786 15 7.5C15 11.6421 11.6421 15 7.5 15C6.46585 15 5.48059 14.7907 4.58427 14.4121L6.49504 10.0447C6.97541 10.6368 7.70586 11 8.5 11C10.433 11 12 9.433 12 7.5V7C12 4.79086 10.2091 3 8 3H7C4.79086 3 3 4.79086 3 7V7.5C3 8.39609 3.33741 9.21457 3.89133 9.83346L4.63646 9.16654C4.2403 8.72391 4 8.14062 4 7.5V7C4 5.34315 5.34315 4 7 4H8C9.65685 4 11 5.34315 11 7V7.5C11 8.88071 9.88071 10 8.5 10C7.81943 10 7.21522 9.56451 7 8.91886L6.99463 8.90274L7.95815 6.70041L7.04199 6.29959L3.68991 13.9615C1.48133 12.6564 0 10.2512 0 7.5Z"
      fill={color}
    />
  {/if}
</svg>

<!--
  @component
  [Go to Document](https://svelte-teenyicons.codewithshin.com/)

  ## Props
  @prop size: string = "15";
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
