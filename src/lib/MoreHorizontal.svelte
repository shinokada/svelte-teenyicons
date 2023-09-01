<script lang="ts">
  export let size: string = "15";
  export let role: string = "img";
  export let color: string = "currentColor" 
  export let variation: "solid" | "outline" = "outline";
export let ariaLabel="more horizontal" </script>

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
    <path d="M3 7.5C3 7.77614 2.77614 8 2.5 8C2.22386 8 2 7.77614 2 7.5C2 7.22386 2.22386 7 2.5 7C2.77614 7 3 7.22386 3 7.5Z" stroke="{color}"/> <path d="M8 7.5C8 7.77614 7.77614 8 7.5 8C7.22386 8 7 7.77614 7 7.5C7 7.22386 7.22386 7 7.5 7C7.77614 7 8 7.22386 8 7.5Z" stroke="{color}"/> <path d="M13 7.5C13 7.77614 12.7761 8 12.5 8C12.2239 8 12 7.77614 12 7.5C12 7.22386 12.2239 7 12.5 7C12.7761 7 13 7.22386 13 7.5Z" stroke="{color}"/> 
  {:else}
    <path fill-rule="evenodd" clip-rule="evenodd" d="M1.5 7.5C1.5 6.94772 1.94772 6.5 2.5 6.5C3.05228 6.5 3.5 6.94772 3.5 7.5C3.5 8.05228 3.05228 8.5 2.5 8.5C1.94772 8.5 1.5 8.05228 1.5 7.5ZM6.5 7.5C6.5 6.94772 6.94772 6.5 7.5 6.5C8.05228 6.5 8.5 6.94772 8.5 7.5C8.5 8.05228 8.05228 8.5 7.5 8.5C6.94772 8.5 6.5 8.05228 6.5 7.5ZM11.5 7.5C11.5 6.94772 11.9477 6.5 12.5 6.5C13.0523 6.5 13.5 6.94772 13.5 7.5C13.5 8.05228 13.0523 8.5 12.5 8.5C11.9477 8.5 11.5 8.05228 11.5 7.5Z" fill="{color}"/> 
  {/if}
</svg>
