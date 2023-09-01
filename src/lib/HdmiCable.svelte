<script lang="ts">
  export let size: string = "15";
  export let role: string = "img";
  export let color: string = "currentColor" 
  export let variation: "solid" | "outline" = "outline";
export let ariaLabel="hdmi cable" </script>

<svg
  xmlns="http://www.w3.org/2000/svg"
  width={size}
  height={size}
  fill="none"
  {...$$restProps}
  {role}
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
    <path d="M3.5 4V0.5H11.5V4M5 2.5H6M9 2.5H10M5.5 13V15M9.5 13V15M2.5 4.5H12.5V9.5L10.5 10.5V12.5H4.5V10.5L2.5 9.5V4.5Z" stroke="{color}"/> 
  {:else}
    <path fill-rule="evenodd" clip-rule="evenodd" d="M3 0H12V5H3V0ZM6 3H5V2H6V3ZM10 3H9V2H10V3Z" fill="{color}"/> <path d="M2 6H13V9.80902L11 10.809V13L10 13V15H9V13H6V15H5V13L4 13V10.809L2 9.80902V6Z" fill="{color}"/> 
  {/if}
</svg>
