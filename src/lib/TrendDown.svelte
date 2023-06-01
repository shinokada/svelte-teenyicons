<script lang="ts">
  export let size: string = '15';
  export let role: string = 'img';
  export let color: string = 'black';
  export let variation: 'solid' | 'outline' = 'outline';
  export let ariaLabel = 'trend down';
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
    <path d="M0.5 3.5L5 8L8 5L14.5 11.5M14.5 11.5V5M14.5 11.5H8" stroke={color} />
  {:else}
    <path
      fill-rule="evenodd"
      clip-rule="evenodd"
      d="M0.146454 3.85353L0.853561 3.14642L5.00001 7.29287L8.00001 4.29287L14 10.2929V4.99998H15V12H8.00001V11H13.2929L8.00001 5.70708L5.00001 8.70708L0.146454 3.85353Z"
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
