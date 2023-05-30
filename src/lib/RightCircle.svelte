<script lang="ts">
  export let size: string = '15';
  export let color: string = 'black';
  export let variation: 'solid' | 'outline' = 'outline';
  export let ariaLabel = 'right circle';
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
      d="M6.14645 10.1464L5.79289 10.5L6.5 11.2071L6.85355 10.8536L6.14645 10.1464ZM9.5 7.5L9.85355 7.85355L10.2071 7.5L9.85355 7.14645L9.5 7.5ZM6.85355 4.14645L6.5 3.79289L5.79289 4.5L6.14645 4.85355L6.85355 4.14645ZM6.85355 10.8536L9.85355 7.85355L9.14645 7.14645L6.14645 10.1464L6.85355 10.8536ZM9.85355 7.14645L6.85355 4.14645L6.14645 4.85355L9.14645 7.85355L9.85355 7.14645ZM7.5 1C11.0899 1 14 3.91015 14 7.5H15C15 3.35787 11.6421 3.57628e-07 7.5 0V1ZM1 7.5C1 3.91015 3.91015 1 7.5 1V0C3.35787 -3.57628e-07 3.57628e-07 3.35786 0 7.5H1ZM7.5 14C3.91015 14 1 11.0899 1 7.5H0C-3.57628e-07 11.6421 3.35786 15 7.5 15V14ZM7.5 15C11.6421 15 15 11.6421 15 7.5H14C14 11.0899 11.0899 14 7.5 14V15Z"
      fill={color}
    />
  {:else}
    <path
      fill-rule="evenodd"
      clip-rule="evenodd"
      d="M15 7.5C15 11.6421 11.6421 15 7.5 15C3.35786 15 0 11.6421 0 7.5C0 3.35786 3.35787 0 7.5 0C11.6421 0 15 3.35786 15 7.5ZM6 3.29285L10.2071 7.49995L6 11.7071V3.29285Z"
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
