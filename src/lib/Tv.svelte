<script lang="ts">
  export let size: string = '15';
  export let color: string = 'black';
  export let variation: 'solid' | 'outline' = 'outline';
  export let ariaLabel = 'tv';
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
      d="M2.5 11.5V13.5M12.5 11.5V13.5M1 13.5H4M11 13.5H14M0.5 2.5L0.5 10.5C0.5 11.0523 0.947715 11.5 1.5 11.5L13.5 11.5C14.0523 11.5 14.5 11.0523 14.5 10.5V2.5C14.5 1.94772 14.0523 1.5 13.5 1.5L1.5 1.5C0.947716 1.5 0.5 1.94772 0.5 2.5Z"
      stroke={color}
    />
  {:else}
    <path
      d="M1.5 1C0.671573 1 0 1.67157 0 2.5V10.5C0 11.3284 0.671573 12 1.5 12H2V13H1V14H4V13H3V12L12 12V13H11V14H14V13H13V12H13.5C14.3284 12 15 11.3284 15 10.5V2.5C15 1.67157 14.3284 1 13.5 1H1.5Z"
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
