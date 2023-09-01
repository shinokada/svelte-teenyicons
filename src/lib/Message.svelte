<script lang="ts">
  export let size: string = "15";
  export let role: string = "img";
  export let color: string = "currentColor" 
  export let variation: "solid" | "outline" = "outline";
export let ariaLabel="message" </script>

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
    <path fill-rule="evenodd" clip-rule="evenodd" d="M5.5 11.4928L7.5 14.4909L9.5 11.4928H13.5C14.053 11.4928 14.5 11.0461 14.5 10.4935V1.49935C14.5 0.946709 14.053 0.5 13.5 0.5H1.5C0.947 0.5 0.5 0.946709 0.5 1.49935V10.4935C0.5 11.0461 0.947 11.4928 1.5 11.4928H5.5Z" stroke="{color}" stroke-linecap="square" stroke-linejoin="round"/> 
  {:else}
    <path d="M1.5 0C0.671165 0 0 0.670259 0 1.49935V10.4935C0 11.3226 0.671165 11.9928 1.5 11.9928H5.2325L7.08406 14.7683C7.1768 14.9074 7.33288 14.9909 7.5 14.9909C7.66712 14.9909 7.8232 14.9074 7.91594 14.7683L9.7675 11.9928H13.5C14.3288 11.9928 15 11.3226 15 10.4935V1.49935C15 0.670259 14.3288 0 13.5 0H1.5Z" fill="{color}"/> 
  {/if}
</svg>
