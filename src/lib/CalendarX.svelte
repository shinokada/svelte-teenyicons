<script lang="ts">
  export let size: string = "15";
  export let color: string = "black" 
  export let variation: "solid" | "outline" = "outline";
export let ariaLabel="calendar x" </script>

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
    <path d="M3.5 0V5M11.5 0V5M5.5 6.5L9.5 10.5M5.5 10.5L9.5 6.5M1.5 2.5H13.5C14.0523 2.5 14.5 2.94772 14.5 3.5V13.5C14.5 14.0523 14.0523 14.5 13.5 14.5H1.5C0.947716 14.5 0.5 14.0523 0.5 13.5V3.5C0.5 2.94772 0.947715 2.5 1.5 2.5Z" stroke="{color}"/> 
  {:else}
    <path fill-rule="evenodd" clip-rule="evenodd" d="M13.5 2H12V0H11V2H4V0H3V2H1.5C0.671573 2 0 2.67157 0 3.5V13.5C0 14.3284 0.671573 15 1.5 15H13.5C14.3284 15 15 14.3284 15 13.5V3.5C15 2.67157 14.3284 2 13.5 2ZM9.14648 10.8535L7.50004 9.20708L5.85359 10.8535L5.14648 10.1464L6.79293 8.49998L5.14648 6.85353L5.85359 6.14642L7.50004 7.79287L9.14648 6.14642L9.85359 6.85353L8.20714 8.49998L9.85359 10.1464L9.14648 10.8535Z" fill="{color}"/> 
  {/if}
</svg>
