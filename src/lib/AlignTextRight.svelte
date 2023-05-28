<script lang="ts">
  export let size: string = "15";
  export let color: string = "black" 
  export let variation: "solid" | "outline" = "outline";
export let ariaLabel="align text right" </script>

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
    <path d="M15 3.5H0M15 11.5H6M15 7.5H9" stroke="{color}"/> 
  {:else}
    <path fill-rule="evenodd" clip-rule="evenodd" d="M0 3H15V4H0V3ZM9 7H15V8H9V7ZM6 11H15V12H6V11Z" fill="{color}"/> 
  {/if}
</svg>
