<script lang="ts">
  export let size: string = "15";
  export let color: string = "black" 
  export let variation: "solid" | "outline" = "outline";
export let ariaLabel="bag plus" </script>

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
    <path d="M4.49998 4V3.5C4.49998 1.84315 5.84313 0.5 7.49998 0.5C9.15683 0.5 10.5 1.84315 10.5 3.5V4M7.49998 7V12M4.99998 9.5H9.99998M2.40114 6.38957L1.62336 13.3896C1.55754 13.9819 2.02123 14.5 2.61724 14.5H12.3827C12.9787 14.5 13.4424 13.9819 13.3766 13.3896L12.5988 6.38957C12.5426 5.88313 12.1145 5.5 11.6049 5.5H3.39502C2.88547 5.5 2.45741 5.88314 2.40114 6.38957Z" stroke="{color}"/> 
  {:else}
    <path d="M5 3.5C5 2.11929 6.11929 1 7.5 1C8.88071 1 10 2.11929 10 3.5V4H11V3.5C11 1.567 9.433 0 7.5 0C5.567 0 4 1.567 4 3.5V4H5V3.5Z" fill="{color}"/> <path fill-rule="evenodd" clip-rule="evenodd" d="M1.90432 6.33435C1.98872 5.5747 2.63082 5 3.39514 5H11.6051C12.3694 5 13.0115 5.5747 13.0959 6.33435L13.8737 13.3344C13.9724 14.2229 13.2769 15 12.3828 15H2.61737C1.72335 15 1.02781 14.2229 1.12654 13.3344L1.90432 6.33435ZM7 9V7H8V9H10V10H8V12H7V10H5V9H7Z" fill="{color}"/> 
  {/if}
</svg>
