<script lang="ts">
  export let size: string = "15";
  export let role: string = "img";
  export let color: string = "currentColor" 
  export let variation: "solid" | "outline" = "outline";
export let ariaLabel="minimise" </script>

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
    <path d="M9.49999 9.5L13 9.5M9.49999 9.5L9.49999 13M9.49999 9.5L13.5 13.5M13 5.5L9.5 5.5M9.5 5.5V2M9.5 5.5L13.5 1.5M2 5.5L5.5 5.5M5.5 5.5L5.5 2M5.5 5.5L1.5 1.5M5.5 13L5.5 9.5M5.5 9.5L2 9.5M5.5 9.5L1.5 13.5" stroke="{color}"/> 
  {:else}
    <path fill-rule="evenodd" clip-rule="evenodd" d="M13.8536 1.85356L10.7071 5.00001L13 5.00001V6.00001L9 6.00001V2.00001H10V4.2929L13.1464 1.14645L13.8536 1.85356ZM4.29289 5.00001L1.14645 1.85356L1.85355 1.14645L5 4.2929L5 2.00001L6 2.00001V6.00001L2 6.00001L2 5.00001L4.29289 5.00001ZM2 9.00001L6 9.00001L6 13H5L5 10.7071L1.85355 13.8536L1.14645 13.1465L4.29289 10L2 10L2 9.00001ZM9 9.00001L13 9.00001V10L10.7071 10L13.8536 13.1465L13.1464 13.8536L9.99999 10.7071L9.99999 13L8.99999 13L9 9.00001Z" fill="{color}"/> 
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