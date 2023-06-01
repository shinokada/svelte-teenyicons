<script lang="ts">
  export let size: string = '15';
  export let role: string = 'img';
  export let color: string = 'black';
  export let variation: 'solid' | 'outline' = 'outline';
  export let ariaLabel = 'x small';
</script>

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
    <path d="M4.5 4.5L10.5 10.5M4.5 10.5L10.5 4.5" stroke={color} />
  {:else}
    <path
      fill-rule="evenodd"
      clip-rule="evenodd"
      d="M6.79289 7.49998L4.14645 4.85353L4.85355 4.14642L7.5 6.79287L10.1464 4.14642L10.8536 4.85353L8.20711 7.49998L10.8536 10.1464L10.1464 10.8535L7.5 8.20708L4.85355 10.8535L4.14645 10.1464L6.79289 7.49998Z"
      fill={color}
    />
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
