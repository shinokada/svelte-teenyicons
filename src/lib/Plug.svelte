<script lang="ts">
  export let size: string = "15";
  export let color: string = "black" 
  export let variation: "solid" | "outline" = "outline";
export let ariaLabel="plug" </script>

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
    <path d="M6.5 11.5V15M8.5 11.5V15M4.5 0V4.5M10.5 0V4.5M2.5 4.5H12.5V7.5H11.5V9.5C11.5 10.6046 10.6046 11.5 9.5 11.5H5.5C4.39543 11.5 3.5 10.6046 3.5 9.5V7.5H2.5V4.5Z" stroke="{color}"/> 
  {:else}
    <path d="M10 4H5V0H4V4H2V8H3V9.5C3 10.8807 4.11929 12 5.5 12H6V15H7V12H8V15H9V12H9.5C10.8807 12 12 10.8807 12 9.5V8H13V4H11V0H10V4Z" fill="{color}"/> 
  {/if}
</svg>
