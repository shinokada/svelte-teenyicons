<script lang="ts">
  export let size: string = "15";
  export let color: string = "black" 
  export let variation: "solid" | "outline" = "outline";
export let ariaLabel="toggle" </script>

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
    <path d="M3.5 2.5C4.05228 2.5 4.5 2.94771 4.5 3.5C4.5 4.05228 4.05228 4.5 3.5 4.5C2.94772 4.5 2.5 4.05228 2.5 3.5C2.5 2.94771 2.94772 2.5 3.5 2.5Z" stroke="{color}"/> <path d="M11.5 0.5H3.5C1.84315 0.5 0.5 1.84315 0.5 3.5C0.5 5.15685 1.84315 6.5 3.5 6.5H11.5C13.1569 6.5 14.5 5.15685 14.5 3.5C14.5 1.84315 13.1569 0.5 11.5 0.5Z" stroke="{color}"/> <path d="M11.5 12.5C10.9477 12.5 10.5 12.0523 10.5 11.5C10.5 10.9477 10.9477 10.5 11.5 10.5C12.0523 10.5 12.5 10.9477 12.5 11.5C12.5 12.0523 12.0523 12.5 11.5 12.5Z" stroke="{color}"/> <path d="M3.5 14.5H11.5C13.1569 14.5 14.5 13.1569 14.5 11.5C14.5 9.84315 13.1569 8.5 11.5 8.5L3.5 8.5C1.84315 8.5 0.5 9.84315 0.5 11.5C0.5 13.1569 1.84315 14.5 3.5 14.5Z" stroke="{color}"/> 
  {:else}
    <path fill-rule="evenodd" clip-rule="evenodd" d="M0 3.5C0 1.567 1.567 0 3.5 0H11.5C13.433 0 15 1.567 15 3.5C15 5.433 13.433 7 11.5 7H3.5C1.567 7 0 5.433 0 3.5ZM3.5 2C4.32843 2 5 2.67157 5 3.5C5 4.32843 4.32843 5 3.5 5C2.67157 5 2 4.32843 2 3.5C2 2.67157 2.67157 2 3.5 2Z" fill="{color}"/> <path fill-rule="evenodd" clip-rule="evenodd" d="M15 11.5C15 13.433 13.433 15 11.5 15L3.5 15C1.567 15 0 13.433 0 11.5C0 9.567 1.567 8 3.5 8L11.5 8C13.433 8 15 9.567 15 11.5ZM11.5 13C10.6716 13 10 12.3284 10 11.5C10 10.6716 10.6716 10 11.5 10C12.3284 10 13 10.6716 13 11.5C13 12.3284 12.3284 13 11.5 13Z" fill="{color}"/> 
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