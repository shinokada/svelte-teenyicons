<script lang="ts">
  export let size: string = "15";
  export let role: string = "img";
  export let color: string = "currentColor" 
  export let variation: "solid" | "outline" = "outline";
export let ariaLabel="keyboard" </script>

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
    <path d="M11 11.5L4 11.5M11 8.5H10M8 8.5H7M5 8.5H4M11 6.5H10M8 6.5H7M5 6.5H4M7.5 4.5V0M13.5 4.5L1.5 4.5C0.947716 4.5 0.500001 4.94771 0.500001 5.5L0.5 12.5C0.5 13.0523 0.947716 13.5 1.5 13.5L13.5 13.5C14.0523 13.5 14.5 13.0523 14.5 12.5V5.5C14.5 4.94772 14.0523 4.5 13.5 4.5Z" stroke="{color}"/> 
  {:else}
    <path fill-rule="evenodd" clip-rule="evenodd" d="M8 0V4H13.5C14.3284 4 15 4.67157 15 5.5V12.5C15 13.3284 14.3284 14 13.5 14L1.5 14C0.671574 14 0 13.3284 0 12.5V5.5C0 4.67157 0.671574 4 1.5 4H7V0H8ZM10 6H11V7H10V6ZM11 8H10V9H11V8ZM11 11H4V12H11V11ZM7 8H8V9H7V8ZM5 8H4V9H5V8ZM8 6H7V7H8V6ZM4 6H5V7H4V6Z" fill="{color}"/> 
  {/if}
</svg>
