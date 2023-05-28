<script lang="ts">
  export let size: string = "15";
  export let color: string = "black" 
  export let variation: "solid" | "outline" = "outline";
export let ariaLabel="envelope open" </script>

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
    <path d="M0.5 5L7.5 8.5L14.5 5M14.5 5.08032V13.5C14.5 14.0523 14.0523 14.5 13.5 14.5H1.5C0.947716 14.5 0.5 14.0523 0.5 13.5V5.08032C0.5 4.72146 0.692286 4.39012 1.00386 4.21208L7.00386 0.783505C7.31129 0.60783 7.68871 0.60783 7.99614 0.783506L13.9961 4.21208C14.3077 4.39012 14.5 4.72146 14.5 5.08032Z" stroke="{color}"/> 
  {:else}
    <path d="M6.75585 0.349399C7.217 0.0858853 7.78312 0.0858856 8.24427 0.349399L14.2443 3.77797C14.4018 3.86798 14.539 3.98411 14.6517 4.11914L7.5 7.93335L0.348436 4.11918C0.461117 3.98413 0.59832 3.86799 0.755853 3.77797L6.75585 0.349399Z" fill="{color}"/> <path d="M0.00012234 5.06674C8.14919e-05 5.07127 6.10352e-05 5.0758 6.10352e-05 5.08034V13.5C6.10352e-05 14.3284 0.671635 15 1.50006 15H13.5001C14.3285 15 15.0001 14.3284 15.0001 13.5V5.08034C15.0001 5.07578 15 5.07123 15 5.06668L7.5 9.06668L0.00012234 5.06674Z" fill="{color}"/> 
  {/if}
</svg>
