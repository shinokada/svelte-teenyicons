<script lang="ts">
  export let size: string = "15";
  export let color: string = "black" 
  export let variation: "solid" | "outline" = "outline";
export let ariaLabel="google drive" </script>

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
    <path d="M5 1.5L0.5 9.5L2.5 13.5M5 1.5L7.5 5.5L2.5 13.5M5 1.5H10L14.5 9.5M5 1.5L10 9.5H14.5M2.5 13.5L5 9.5H14.5M2.5 13.5H12.5L14.5 9.5" stroke="{color}" stroke-linejoin="round"/> 
  {:else}
    <path d="M4.56268 1.25762C4.65079 1.09864 4.81824 1 5 1H10C10.1806 1 10.3472 1.09743 10.4358 1.25487L14.2299 8H8.47288L4.576 1.765C4.47967 1.61087 4.47457 1.41659 4.56268 1.25762Z" fill="{color}"/> <path d="M3.91064 14H12.4999C12.6893 14 12.8624 13.893 12.9471 13.7236L14.9471 9.72361C15.0246 9.56861 15.0163 9.38454 14.9252 9.23713C14.8341 9.08973 14.6732 9 14.4999 9H7.09246L3.91064 14Z" fill="{color}"/> <path d="M0.0642124 9.25481L3.85624 2.51343L6.90622 7.39339L2.924 13.7649C2.82814 13.9183 2.65693 14.008 2.47627 13.9994C2.29561 13.9908 2.13367 13.8853 2.05279 13.7236L0.0527865 9.72355C-0.021442 9.57509 -0.0171613 9.39948 0.0642124 9.25481Z" fill="{color}"/> 
  {/if}
</svg>
