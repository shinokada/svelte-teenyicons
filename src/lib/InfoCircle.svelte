<script lang="ts">
  export let size: string = '15';
  export let role: string = 'img';
  export let color: string = 'black';
  export let variation: 'solid' | 'outline' = 'outline';
  export let ariaLabel = 'info circle';
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
      d="M7 4.5V5H8V4.5H7ZM8 4.49V3.99H7V4.49H8ZM8 11V7H7V11H8ZM8 4.5V4.49H7V4.5H8ZM6 8H7.5V7H6V8ZM6 11H9V10H6V11ZM7.5 1C11.0899 1 14 3.91015 14 7.5H15C15 3.35787 11.6421 3.57628e-07 7.5 0V1ZM1 7.5C1 3.91015 3.91015 1 7.5 1V0C3.35787 -3.57628e-07 3.57628e-07 3.35786 0 7.5H1ZM7.5 14C3.91015 14 1 11.0899 1 7.5H0C-3.57628e-07 11.6421 3.35786 15 7.5 15V14ZM7.5 15C11.6421 15 15 11.6421 15 7.5H14C14 11.0899 11.0899 14 7.5 14V15Z"
      fill={color}
    />
  {:else}
    <path
      fill-rule="evenodd"
      clip-rule="evenodd"
      d="M15 7.5C15 11.6421 11.6421 15 7.5 15C3.35786 15 0 11.6421 0 7.5C0 3.35786 3.35787 0 7.5 0C11.6421 0 15 3.35786 15 7.5ZM7 4.99999V3.98999H8V4.99999H7ZM8 6.99999V9.99999H9V11H6V9.99999H7V7.99999H6V6.99999H8Z"
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
