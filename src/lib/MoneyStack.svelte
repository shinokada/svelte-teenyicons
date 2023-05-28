<script lang="ts">
  export let size: string = "15";
  export let color: string = "black" 
  export let variation: "solid" | "outline" = "outline";
export let ariaLabel="money stack" </script>

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
    <path d="M0 12.5H15M0 14.5H15M2.5 4V2.5H4M11 2.5H12.5V4M2.5 7V8.5H4M11 8.5H12.5V7M7.5 7.5C6.39543 7.5 5.5 6.60457 5.5 5.5C5.5 4.39543 6.39543 3.5 7.5 3.5C8.60457 3.5 9.5 4.39543 9.5 5.5C9.5 6.60457 8.60457 7.5 7.5 7.5ZM1.5 0.5H13.5C14.0523 0.5 14.5 0.947715 14.5 1.5V9.5C14.5 10.0523 14.0523 10.5 13.5 10.5H1.5C0.947716 10.5 0.5 10.0523 0.5 9.5V1.5C0.5 0.947716 0.947715 0.5 1.5 0.5Z" stroke="{color}"/> 
  {:else}
    <path d="M6 5.5C6 4.67157 6.67157 4 7.5 4C8.32843 4 9 4.67157 9 5.5C9 6.32843 8.32843 7 7.5 7C6.67157 7 6 6.32843 6 5.5Z" fill="{color}"/> <path fill-rule="evenodd" clip-rule="evenodd" d="M1.5 0C0.671573 0 0 0.671573 0 1.5V9.5C0 10.3284 0.671574 11 1.5 11H13.5C14.3284 11 15 10.3284 15 9.5V1.5C15 0.671573 14.3284 0 13.5 0H1.5ZM4 2H2V4H3V3H4V2ZM7.5 3C6.11929 3 5 4.11929 5 5.5C5 6.88071 6.11929 8 7.5 8C8.88071 8 10 6.88071 10 5.5C10 4.11929 8.88071 3 7.5 3ZM12 3H11V2H13V4H12V3ZM3 7H2V9H4V8H3V7ZM11 9V8H12V7H13V9H11Z" fill="{color}"/> <path d="M0 12V13H15V12H0Z" fill="{color}"/> <path d="M0 14V15H15V14H0Z" fill="{color}"/> 
  {/if}
</svg>
