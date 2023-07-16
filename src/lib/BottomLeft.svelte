<script lang="ts">
  export let size: string = '15';
  export let role: string = 'img';
  export let color: string = 'currentColor';
  export let variation: 'solid' | 'outline' = 'outline';
  export let ariaLabel = 'bottom left';
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
      d="M1.5 13.5H1C1 13.7761 1.22386 14 1.5 14V13.5ZM1.5 14H6.99999V13H1.5V14ZM2 13.5V8H1V13.5H2ZM1.85355 13.8536L13.8535 1.85355L13.1464 1.14645L1.14645 13.1464L1.85355 13.8536Z"
      fill={color}
    />
  {:else}
    <path
      fill-rule="evenodd"
      clip-rule="evenodd"
      d="M13.8536 1.85356L2.70711 13H7V14H1.00001V8.00001H2.00001V12.2929L13.1464 1.14645L13.8536 1.85356Z"
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
