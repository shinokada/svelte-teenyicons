<script lang="ts">
  export let size: string = '15';
  export let color: string = 'black';
  export let variation: 'solid' | 'outline' = 'outline';
  export let ariaLabel = 'screen';
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
      d="M4 14.5H11M0.5 2.5L0.5 10.5C0.5 11.0523 0.947716 11.5 1.5 11.5L13.5 11.5C14.0523 11.5 14.5 11.0523 14.5 10.5V2.5C14.5 1.94772 14.0523 1.5 13.5 1.5L1.5 1.5C0.947716 1.5 0.5 1.94772 0.5 2.5Z"
      stroke={color}
    />
  {:else}
    <path
      d="M1.5 1C0.671573 1 0 1.67157 0 2.5V10.5C0 11.3284 0.671574 12 1.5 12L13.5 12C14.3284 12 15 11.3284 15 10.5V2.5C15 1.67157 14.3284 1 13.5 1H1.5Z"
      fill={color}
    /> <path d="M4 15H11V14H4V15Z" fill={color} />
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
