<script lang="ts">
  export let size: string = "15";
  export let role: string = "img";
  export let color: string = "currentColor" 
  export let variation: "solid" | "outline" = "outline";
export let ariaLabel="list layout" </script>

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
    <path d="M7 3.5H15M7 11.5H15M1.5 1.5H3.5C4.05228 1.5 4.5 1.94772 4.5 2.5V4.5C4.5 5.05228 4.05228 5.5 3.5 5.5H1.5C0.947715 5.5 0.5 5.05228 0.5 4.5V2.5C0.5 1.94772 0.947715 1.5 1.5 1.5ZM1.5 9.5H3.5C4.05228 9.5 4.5 9.94772 4.5 10.5V12.5C4.5 13.0523 4.05228 13.5 3.5 13.5H1.5C0.947715 13.5 0.5 13.0523 0.5 12.5V10.5C0.5 9.94772 0.947715 9.5 1.5 9.5Z" stroke="{color}"/> 
  {:else}
    <path d="M1.5 1C0.671573 1 0 1.67157 0 2.5V4.5C0 5.32843 0.671573 6 1.5 6H3.5C4.32843 6 5 5.32843 5 4.5V2.5C5 1.67157 4.32843 1 3.5 1H1.5Z" fill="{color}"/> <path d="M7 4H15V3H7V4Z" fill="{color}"/> <path d="M1.5 9C0.671573 9 0 9.67157 0 10.5V12.5C0 13.3284 0.671573 14 1.5 14H3.5C4.32843 14 5 13.3284 5 12.5V10.5C5 9.67157 4.32843 9 3.5 9H1.5Z" fill="{color}"/> <path d="M7 12H15V11H7V12Z" fill="{color}"/> 
  {/if}
</svg>
