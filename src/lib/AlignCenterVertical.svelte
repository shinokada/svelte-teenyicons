<script lang="ts">
  export let size: string = "15";
  export let color: string = "black" 
  export let variation: "solid" | "outline" = "outline";
export let ariaLabel="align center vertical" </script>

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
    <path d="M15 7.5H11.5M3.5 7.5H0M8.5 7.5H6.5M11.5 11H8.5V4H11.5V11ZM6.5 13.5H3.5V1.5H6.5V13.5Z" stroke="{color}"/> 
  {:else}
    <path d="M7 1H3V7H0V8H3V14H7V8H8V11.5H12V8H15V7H12V3.5H8V7H7V1Z" fill="{color}"/> 
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