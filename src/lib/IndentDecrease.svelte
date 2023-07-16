<script lang="ts">
  export let size: string = "15";
  export let role: string = "img";
  export let color: string = "currentColor" 
  export let variation: "solid" | "outline" = "outline";
export let ariaLabel="indent decrease" </script>

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
    <path d="M0.5 7.5L0.146447 7.14645C-0.0488155 7.34171 -0.0488155 7.65829 0.146447 7.85355L0.5 7.5ZM3 4H15V3H3V4ZM7 8H15V7H7V8ZM3 12H15V11H3V12ZM2.85355 9.14645L0.853553 7.14645L0.146447 7.85355L2.14645 9.85355L2.85355 9.14645ZM0.853553 7.85355L2.85355 5.85355L2.14645 5.14645L0.146447 7.14645L0.853553 7.85355Z" fill="{color}"/> 
  {:else}
    <path fill-rule="evenodd" clip-rule="evenodd" d="M15 4H3V3H15V4ZM1.20711 7.5L2.85355 5.85355L2.14645 5.14645L0.146447 7.14645C-0.0488155 7.34171 -0.0488155 7.65829 0.146447 7.85355L2.14645 9.85355L2.85355 9.14645L1.20711 7.5ZM15 8H7V7H15V8ZM15 12H3V11H15V12Z" fill="{color}"/> 
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