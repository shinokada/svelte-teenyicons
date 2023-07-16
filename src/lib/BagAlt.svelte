<script lang="ts">
  export let size: string = "15";
  export let role: string = "img";
  export let color: string = "currentColor" 
  export let variation: "solid" | "outline" = "outline";
export let ariaLabel="bag alt" </script>

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
    <path d="M10.5 2L10.5 4.5C10.5 6.15685 9.15685 7.5 7.5 7.5C5.84315 7.5 4.5 6.15685 4.5 4.5L4.5 2M1.5 1.5V13.5C1.5 14.0523 1.94772 14.5 2.5 14.5H12.5C13.0523 14.5 13.5 14.0523 13.5 13.5V1.5C13.5 0.947716 13.0523 0.5 12.5 0.5H2.5C1.94772 0.5 1.5 0.947715 1.5 1.5Z" stroke="{color}"/> 
  {:else}
    <path fill-rule="evenodd" clip-rule="evenodd" d="M1 1.5C1 0.671573 1.67157 0 2.5 0H12.5C13.3284 0 14 0.671573 14 1.5V13.5C14 14.3284 13.3284 15 12.5 15H2.5C1.67157 15 1 14.3284 1 13.5V1.5ZM10 4.5C10 5.88071 8.88071 7 7.5 7C6.11929 7 5 5.88071 5 4.5V2L4 2L4 4.5C4 6.433 5.567 8 7.5 8C9.433 8 11 6.433 11 4.5V2H10V4.5Z" fill="{color}"/> 
  {/if}
</svg>


<!--
  @component
  [Go to Document](https://svelte-teenyicons.codewithshin.com/)

  ## Props
  @prop size: string = "15";
  @prop role: string = "icon file name";
  @prop color: string = "black" 
  @prop variation: "solid" | "outline" = "outline";
  @prop ariaLabel = 'icon file name';
  ## Event
  - on:click 
  - on:mouseenter 
  - on:mouseleave 
  - on:mouseover 
  - on:mouseout 
  - on:blur 
  - on:focus 
-->