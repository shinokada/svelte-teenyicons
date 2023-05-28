<script lang="ts">
  export let size: string = "15";
  export let color: string = "black" 
  export let variation: "solid" | "outline" = "outline";
export let ariaLabel="bold" </script>

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
    <path d="M3.5 7.5H8.5C10.1569 7.5 11.5 6.15685 11.5 4.5C11.5 2.84315 10.1569 1.5 8.5 1.5H3.57921C3.53546 1.5 3.5 1.53546 3.5 1.57921V7.5ZM3.5 7.5H9.5C11.1569 7.5 12.5 8.84315 12.5 10.5C12.5 12.1569 11.1569 13.5 9.5 13.5H3.58911C3.53989 13.5 3.5 13.4601 3.5 13.4109V7.5Z" stroke="{color}"/> 
  {:else}
    <path fill-rule="evenodd" clip-rule="evenodd" d="M3 1.57921C3 1.25932 3.25932 1 3.57921 1H8.5C10.433 1 12 2.567 12 4.5C12 5.59515 11.497 6.57282 10.7095 7.2146C12.0465 7.70695 13 8.99212 13 10.5C13 12.433 11.433 14 9.5 14H3.58911C3.26374 14 3 13.7362 3 13.4109V1.57921ZM4 8V13H9.5C10.8807 13 12 11.8807 12 10.5C12 9.11929 10.8807 8 9.5 8H4ZM4 7H8.5C9.88071 7 11 5.88071 11 4.5C11 3.11929 9.88071 2 8.5 2H4V7Z" fill="{color}"/> 
  {/if}
</svg>
