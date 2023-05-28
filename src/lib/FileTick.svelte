<script lang="ts">
  export let size: string = "15";
  export let color: string = "black" 
  export let variation: "solid" | "outline" = "outline";
export let ariaLabel="file tick" </script>

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
    <path d="M5 7.5L7 9.5L10.5 5.5M10.5 0.5H2.5C1.94772 0.5 1.5 0.947716 1.5 1.5V13.5C1.5 14.0523 1.94772 14.5 2.5 14.5H12.5C13.0523 14.5 13.5 14.0523 13.5 13.5V3.5L10.5 0.5Z" stroke="{color}"/> 
  {:else}
    <path fill-rule="evenodd" clip-rule="evenodd" d="M1 1.5C1 0.671573 1.67157 0 2.5 0H10.7071L14 3.29289V13.5C14 14.3284 13.3284 15 12.5 15H2.5C1.67157 15 1 14.3284 1 13.5V1.5ZM7.02439 10.2315L10.8763 5.82928L10.1237 5.17078L6.97568 8.76857L5.35359 7.14648L4.64648 7.85358L7.02439 10.2315Z" fill="{color}"/> 
  {/if}
</svg>
