<script lang="ts">
  export let size: string = "15";
  export let color: string = "black" 
  export let variation: "solid" | "outline" = "outline";
export let ariaLabel="text" </script>

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
    <path d="M7.5 14V1.5M1.5 5V1.5H13.5V5M3.5 13.5H11" stroke="{color}"/> 
  {:else}
    <path fill-rule="evenodd" clip-rule="evenodd" d="M1 1H14V5H13V2H8V13H11V14H3.5V13H7V2H2V5H1V1Z" fill="{color}"/> 
  {/if}
</svg>
