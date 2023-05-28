<script lang="ts">
  export let size: string = "15";
  export let color: string = "black" 
  export let variation: "solid" | "outline" = "outline";
export let ariaLabel="wallet" </script>

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
    <path d="M0.5 3.5L0.5 12.5C0.5 13.0523 0.947716 13.5 1.5 13.5L13.5 13.5C14.0523 13.5 14.5 13.0523 14.5 12.5V4.5C14.5 3.94772 14.0523 3.5 13.5 3.5L3 3.5M0.5 3.5V2.5C0.5 1.94772 0.947716 1.5 1.5 1.5H9.5C10.0523 1.5 10.5 1.94772 10.5 2.5V3.5L3 3.5M0.5 3.5L3 3.5M9 9.5H12" stroke="{color}"/> 
  {:else}
    <path fill-rule="evenodd" clip-rule="evenodd" d="M0 2.5C0 1.67157 0.671573 1 1.5 1H9.5C10.3284 1 11 1.67157 11 2.5V3L13.5 3C14.3284 3 15 3.67157 15 4.5V12.5C15 13.3284 14.3284 14 13.5 14L1.5 14C0.671573 14 0 13.3284 0 12.5V2.5ZM9 10H12V9H9V10Z" fill="{color}"/> 
  {/if}
</svg>
