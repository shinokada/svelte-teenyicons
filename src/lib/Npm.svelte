<script lang="ts">
  export let size: string = "15";
  export let color: string = "black" 
  export let variation: "solid" | "outline" = "outline";
export let ariaLabel="npm" </script>

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
    <path d="M4.5 10.5V12.5H6.5V10.5H14.5V4.5H0.5V10.5H4.5ZM4.5 10.5V4.5M8.5 4.5V10.5M6.5 6V9M2.5 6V10.5M10.5 6V10.5M12.5 6V10.5" stroke="{color}"/> 
  {:else}
    <path fill-rule="evenodd" clip-rule="evenodd" d="M0 4H15V11H7V13H4V11H0V4ZM4 10V5H1V10H2V6H3V10H4ZM5 5V12H6V10H8V5H5ZM9 5V10H10V6H11V10H12V6H13V10H14V5H9ZM6 9V6H7V9H6Z" fill="{color}"/> 
  {/if}
</svg>
