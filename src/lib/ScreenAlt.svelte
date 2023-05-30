<script lang="ts">
  export let size: string = "15";
  export let color: string = "black" 
  export let variation: "solid" | "outline" = "outline";
export let ariaLabel="screen alt" </script>

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
    <path d="M2 14.5H13M7.5 10.5V14.5M0.5 1.5L0.5 9.5C0.5 10.0523 0.947716 10.5 1.5 10.5L13.5 10.5C14.0523 10.5 14.5 10.0523 14.5 9.5V1.5C14.5 0.947716 14.0523 0.500001 13.5 0.500001L1.5 0.5C0.947716 0.5 0.5 0.947716 0.5 1.5Z" stroke="{color}"/> 
  {:else}
    <path d="M1.5 0C0.671573 0 0 0.671573 0 1.5V9.5C0 10.3284 0.671574 11 1.5 11H7V14H2V15H13V14H8V11H13.5C14.3284 11 15 10.3284 15 9.5V1.5C15 0.671574 14.3284 0 13.5 0H1.5Z" fill="{color}"/> 
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