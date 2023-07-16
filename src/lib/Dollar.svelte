<script lang="ts">
  export let size: string = "15";
  export let role: string = "img";
  export let color: string = "currentColor" 
  export let variation: "solid" | "outline" = "outline";
export let ariaLabel="dollar" </script>

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
    <path d="M2.5 10.5C2.5 12.1569 3.84315 13.5 5.5 13.5H9.5C11.1569 13.5 12.5 12.1569 12.5 10.5C12.5 8.84315 11.1569 7.5 9.5 7.5H5.5C3.84315 7.5 2.5 6.15685 2.5 4.5C2.5 2.84315 3.84315 1.5 5.5 1.5H9.5C11.1569 1.5 12.5 2.84315 12.5 4.5M7.5 0V1.5M7.5 15V13.5" stroke="{color}"/> 
  {:else}
    <path fill-rule="evenodd" clip-rule="evenodd" d="M7 1V0H8V1H9.5C11.433 1 13 2.567 13 4.5H12C12 3.11929 10.8807 2 9.5 2H5.5C4.11929 2 3 3.11929 3 4.5C3 5.88071 4.11929 7 5.5 7H9.5C11.433 7 13 8.567 13 10.5C13 12.433 11.433 14 9.5 14H8V15H7V14H5.5C3.567 14 2 12.433 2 10.5H3C3 11.8807 4.11929 13 5.5 13H9.5C10.8807 13 12 11.8807 12 10.5C12 9.11929 10.8807 8 9.5 8H5.5C3.567 8 2 6.433 2 4.5C2 2.567 3.567 1 5.5 1H7Z" fill="{color}"/> 
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