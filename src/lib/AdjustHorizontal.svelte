<script lang="ts">
  export let size: string = "15";
  export let role: string = "img";
  export let color: string = "currentColor" 
  export let variation: "solid" | "outline" = "outline";
export let ariaLabel="adjust horizontal" </script>

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
    <path d="M2.5 7.5H0M15 12.5L12.5 12.5M15 2.5L8.5 2.50001M6.5 2.5L1.17223e-06 2.5M4.5 7.5L15 7.5M10.5 12.5H7.35117e-07M10.5 10.5V14.5L12.5 14.5V10.5L10.5 10.5ZM2.5 5.5V9.5H4.5V5.5H2.5ZM6.5 0.5L6.5 4.5H8.5V0.5L6.5 0.5Z" stroke="{color}"/> 
  {:else}
    <path d="M9.00001 1.31134e-07L6.00001 0L6.00001 2L7.89166e-06 2L7.84795e-06 3L6.00001 3V5H9.00001V3.00001L15 3L15 2L9.00001 2.00001V1.31134e-07Z" fill="{color}"/> <path d="M5.00001 5H2.00001L2.00001 7L7.67311e-06 7L7.62939e-06 8L2.00001 8L2.00001 10L5.00001 10V8L15 8V7L5.00001 7V5Z" fill="{color}"/> <path d="M13 10L10 10V12L8.40822e-06 12L8.36451e-06 13L10 13V15L13 15V13L15 13V12L13 12V10Z" fill="{color}"/> 
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