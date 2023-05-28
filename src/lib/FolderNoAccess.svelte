<script lang="ts">
  export let size: string = "15";
  export let color: string = "black" 
  export let variation: "solid" | "outline" = "outline";
export let ariaLabel="folder no access" </script>

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
    <path d="M9.5 6.5L5.5 10.5M0.5 2.5V12.5C0.5 13.0523 0.947715 13.5 1.5 13.5H13.5C14.0523 13.5 14.5 13.0523 14.5 12.5V4.5C14.5 3.94772 14.0523 3.5 13.5 3.5H7.5L5.5 1.5H1.5C0.947715 1.5 0.5 1.94772 0.5 2.5ZM7.5 11.5C5.84315 11.5 4.5 10.1569 4.5 8.5C4.5 6.84315 5.84315 5.5 7.5 5.5C9.15685 5.5 10.5 6.84315 10.5 8.5C10.5 10.1569 9.15685 11.5 7.5 11.5Z" stroke="{color}"/> 
  {:else}
    <path d="M7.5 6C6.11929 6 5 7.11929 5 8.5C5 9.00956 5.15245 9.48351 5.41423 9.87874L8.87874 6.41423C8.48351 6.15245 8.00956 6 7.5 6Z" fill="{color}"/> <path d="M7.5 11C6.99048 11 6.51656 10.8476 6.12135 10.5858L9.58583 7.12135C9.84757 7.51656 10 7.99048 10 8.5C10 9.88071 8.88071 11 7.5 11Z" fill="{color}"/> <path fill-rule="evenodd" clip-rule="evenodd" d="M0 2.5C0 1.67157 0.671573 1 1.5 1H5.70711L7.70711 3H13.5C14.3284 3 15 3.67157 15 4.5V12.5C15 13.3284 14.3284 14 13.5 14H1.5C0.671573 14 0 13.3284 0 12.5V2.5ZM4 8.5C4 6.567 5.567 5 7.5 5C9.433 5 11 6.567 11 8.5C11 10.433 9.433 12 7.5 12C5.567 12 4 10.433 4 8.5Z" fill="{color}"/> 
  {/if}
</svg>
