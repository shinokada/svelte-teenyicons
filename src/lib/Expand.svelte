<script lang="ts">
  export let size: string = "15";
  export let role: string = "img";
  export let color: string = "currentColor" 
  export let variation: "solid" | "outline" = "outline";
export let ariaLabel="expand" </script>

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
    <path d="M13.5 13.5H10M13.5 13.5L13.5 10M13.5 13.5L9.5 9.5M10 1.5H13.5M13.5 1.5V5M13.5 1.5L9.5 5.5M5 1.5H1.5M1.5 1.5V5M1.5 1.5L5.5 5.5M1.5 10V13.5M1.5 13.5H5M1.5 13.5L5.5 9.5" stroke="{color}"/> 
  {:else}
    <path fill-rule="evenodd" clip-rule="evenodd" d="M1 1H5V2H2.70711L5.85355 5.14645L5.14645 5.85355L2 2.70711V5H1V1ZM12.2929 2H10V1H14V5H13V2.70711L9.85355 5.85355L9.14645 5.14645L12.2929 2ZM5.85355 9.85355L2.70711 13H5V14H1V10H2V12.2929L5.14645 9.14645L5.85355 9.85355ZM9.85355 9.14645L13 12.2929L13 10L14 10L14 14H10V13H12.2929L9.14645 9.85355L9.85355 9.14645Z" fill="{color}"/> 
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