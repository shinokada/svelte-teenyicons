<script lang="ts">
  export let size: string = '15';
  export let role: string = 'img';
  export let color: string = 'black';
  export let variation: 'solid' | 'outline' = 'outline';
  export let ariaLabel = 'minimise alt';
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
    <path
      d="M13 5.5L9.5 5.5M9.5 5.5V2M9.5 5.5L13.5 1.5M5.5 13L5.5 9.5M5.5 9.5L2 9.5M5.5 9.5L1.5 13.5"
      stroke={color}
    />
  {:else}
    <path
      fill-rule="evenodd"
      clip-rule="evenodd"
      d="M13.8536 1.85356L10.7071 5.00001L13 5.00001V6.00001L9.00001 6.00001V2.00001H10V4.2929L13.1465 1.14645L13.8536 1.85356ZM2.00001 9.00001L6.00001 9.00001L6.00001 13H5.00001L5.00001 10.7071L1.85356 13.8536L1.14645 13.1465L4.2929 10L2.00001 10L2.00001 9.00001Z"
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
