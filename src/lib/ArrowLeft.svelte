<script lang="ts">
  export let size: string = "15";
  export let color: string = "black" 
  export let variation: "solid" | "outline" = "outline";
export let ariaLabel="arrow left" </script>

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
    <path d="M1.5 7.5L5.5 3.5M1.5 7.5L5.5 11.5M1.5 7.5H14" stroke="{color}"/> 
  {:else}
    <path fill-rule="evenodd" clip-rule="evenodd" d="M2.70712 7.99998L5.85357 11.1464L5.14646 11.8535L0.792908 7.49998L5.14646 3.14642L5.85357 3.85353L2.70712 6.99998H14V7.99998H2.70712Z" fill="{color}"/> 
  {/if}
</svg>
