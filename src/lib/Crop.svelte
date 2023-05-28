<script lang="ts">
  export let size: string = "15";
  export let color: string = "black" 
  export let variation: "solid" | "outline" = "outline";
export let ariaLabel="crop" </script>

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
    <path d="M3.5 3.5H11.5V11.5M3.5 3.5V0M3.5 3.5H0M11.5 11.5H3.5V6M11.5 11.5V15M11.5 11.5H15" stroke="{color}"/> 
  {:else}
    <path fill-rule="evenodd" clip-rule="evenodd" d="M3 3V0H4V3H12V11H15V12H12V15H11V12H3V6H4V11H11V4H0V3H3Z" fill="{color}"/> 
  {/if}
</svg>
