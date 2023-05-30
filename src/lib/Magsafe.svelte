<script lang="ts">
  export let size: string = "15";
  export let color: string = "black" 
  export let variation: "solid" | "outline" = "outline";
export let ariaLabel="magsafe" </script>

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
    <path d="M3.5 2.5V0.5H11.5V2.5M5.5 11.5V15M9.5 11.5V15M4.5 9.5V11.5H10.5V9.5M1.5 2.5H13.5V9.5H1.5V2.5Z" stroke="{color}"/> 
  {:else}
    <path d="M12 0H3V3H12V0Z" fill="{color}"/> <path d="M14 4H1V10H4V12H5V15H6V12H9V15H10V12H11V10H14V4Z" fill="{color}"/> 
  {/if}
</svg>


<!--
  @component
  [Go to Document](https://svelte-teenyicons.codewithshin.com/)

  ## Props
  @prop size: string = "15";
  @prop color: string = "black" 
  @prop variation: "solid" | "outline" = "outline";
-->