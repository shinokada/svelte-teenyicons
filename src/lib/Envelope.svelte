<script lang="ts">
  export let size: string = '15';
  export let color: string = 'black';
  export let variation: 'solid' | 'outline' = 'outline';
  export let ariaLabel = 'envelope';
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
      d="M0.5 4.5L7.5 8.5L14.5 4.5M1.5 1.5H13.5C14.0523 1.5 14.5 1.94772 14.5 2.5V12.5C14.5 13.0523 14.0523 13.5 13.5 13.5H1.5C0.947716 13.5 0.5 13.0523 0.5 12.5V2.5C0.5 1.94772 0.947715 1.5 1.5 1.5Z"
      stroke={color}
    />
  {:else}
    <path
      d="M0.5 2.5C0.5 1.67157 1.17157 1 2 1H14C14.8284 1 15.5 1.67157 15.5 2.5V3.70758L8.00001 7.92632L0.5 3.70757V2.5Z"
      fill={color}
    />
    <path
      d="M0.5 4.85491V12.5C0.5 13.3284 1.17157 14 2 14H14C14.8284 14 15.5 13.3284 15.5 12.5V4.85493L8.00001 9.07367L0.5 4.85491Z"
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
