<script lang="ts">
  export let size: string = '15';
  export let color: string = 'black';
  export let variation: 'solid' | 'outline' = 'outline';
  export let ariaLabel = 'double caret right';
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
    <path d="M7 14L14 7.5L7 1M1.5 14L8.5 7.5L1.5 1" stroke={color} stroke-linecap="square" />
  {:else}
    <path
      fill-rule="evenodd"
      clip-rule="evenodd"
      d="M1.47383 0.293396L9.23481 7.50002L1.47383 14.7066L0.793381 13.9738L7.7652 7.50002L0.793381 1.02619L1.47383 0.293396ZM6.97383 0.293396L14.7348 7.50002L6.97383 14.7066L6.29338 13.9738L13.2652 7.50002L6.29338 1.02619L6.97383 0.293396Z"
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
