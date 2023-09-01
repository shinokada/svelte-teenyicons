<script lang="ts">
  export let size: string = "15";
  export let role: string = "img";
  export let color: string = "currentColor" 
  export let variation: "solid" | "outline" = "outline";
export let ariaLabel="line" </script>

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
    <path d="M2 2L13 13M1.5 2.5C0.947715 2.5 0.5 2.05228 0.5 1.5C0.5 0.947715 0.947715 0.5 1.5 0.5C2.05228 0.5 2.5 0.947715 2.5 1.5C2.5 2.05228 2.05228 2.5 1.5 2.5ZM13.5 14.5C12.9477 14.5 12.5 14.0523 12.5 13.5C12.5 12.9477 12.9477 12.5 13.5 12.5C14.0523 12.5 14.5 12.9477 14.5 13.5C14.5 14.0523 14.0523 14.5 13.5 14.5Z" stroke="{color}"/> 
  {:else}
    <path d="M1.5 0C0.671573 0 0 0.671573 0 1.5C0 2.32843 0.671573 3 1.5 3C1.73157 3 1.95089 2.94752 2.14671 2.85381L12.1462 12.8533C12.0525 13.0491 12 13.2684 12 13.5C12 14.3284 12.6716 15 13.5 15C14.3284 15 15 14.3284 15 13.5C15 12.6716 14.3284 12 13.5 12C13.2684 12 13.0491 12.0525 12.8533 12.1462L2.85381 2.14671C2.94752 1.95089 3 1.73157 3 1.5C3 0.671573 2.32843 0 1.5 0Z" fill="{color}"/> 
  {/if}
</svg>
