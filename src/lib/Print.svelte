<script lang="ts">
  export let size: string = "15";
  export let color: string = "black" 
  export let variation: "solid" | "outline" = "outline";
export let ariaLabel="print" </script>

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
    <path d="M3.5 12.5H1.5C0.947715 12.5 0.5 12.0523 0.5 11.5V7.5C0.5 6.94772 0.947715 6.5 1.5 6.5H13.5C14.0523 6.5 14.5 6.94772 14.5 7.5V11.5C14.5 12.0523 14.0523 12.5 13.5 12.5H11.5M3.5 6.5V1.5C3.5 0.947715 3.94772 0.5 4.5 0.5H10.5C11.0523 0.5 11.5 0.947715 11.5 1.5V6.5M3.5 10.5H11.5V14.5H3.5V10.5Z" stroke="{color}"/> 
  {:else}
    <path d="M3 1.5C3 0.671573 3.67157 0 4.5 0H10.5C11.3284 0 12 0.671573 12 1.5V5H3V1.5Z" fill="{color}"/> <path d="M1.5 6C0.671573 6 0 6.67157 0 7.5V11.5C0 12.3284 0.671573 13 1.5 13H2V9H13V13H13.5C14.3284 13 15 12.3284 15 11.5V7.5C15 6.67157 14.3284 6 13.5 6H1.5Z" fill="{color}"/> <path d="M3 10H12V15H3V10Z" fill="{color}"/> 
  {/if}
</svg>
