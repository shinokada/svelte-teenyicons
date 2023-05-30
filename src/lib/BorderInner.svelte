<script lang="ts">
  export let size: string = '15';
  export let color: string = 'black';
  export let variation: 'solid' | 'outline' = 'outline';
  export let ariaLabel = 'border inner';
</script>

<svg
  xmlns="http://www.w3.org/2000/svg"
  width={size}
  height={size}
  fill="none"
  class={$$props.class}
  {...$$restProps}
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
      d="M1 1.5H2M10 1.5H11M13 1.5H14M13 4.5H14M13 10.5H14M13 13.5H14M10 13.5H11M4 13.5H5M1 13.5H2M1 10.5H2M1 4.5H2M4 1.5H5M1 7.5H14M7.5 1V14"
      stroke={color}
    />
  {:else}
    <path
      fill-rule="evenodd"
      clip-rule="evenodd"
      d="M2 2H1V1H2V2ZM5 2H4V1H5V2ZM7 7H1V8H7V14H8V8H14V7H8V1H7V7ZM11 2H10V1H11V2ZM14 2H13V1H14V2ZM2 5H1V4H2V5ZM14 5H13V4H14V5ZM2 11H1V10H2V11ZM14 11H13V10H14V11ZM2 14H1V13H2V14ZM5 14H4V13H5V14ZM11 14H10V13H11V14ZM14 14H13V13H14V14Z"
      fill={color}
    />
  {/if}
</svg>

<!--
  @component
  [Go to Document](https://svelte-teenyicons.codewithshin.com/)

  ## Props
  @prop size: string = "15";
  @prop color: string = "black" 
  @prop variation: "solid" | "outline" = "outline";
-->
