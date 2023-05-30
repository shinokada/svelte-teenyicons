<script lang="ts">
  export let size: string = '15';
  export let color: string = 'black';
  export let variation: 'solid' | 'outline' = 'outline';
  export let ariaLabel = 'servers';
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
      d="M13.5 5.5H1.5M13.5 5.5C14.0523 5.5 14.5 5.05228 14.5 4.5V2.5C14.5 1.94772 14.0523 1.5 13.5 1.5H1.5C0.947715 1.5 0.5 1.94772 0.5 2.5V4.5C0.5 5.05228 0.947716 5.5 1.5 5.5M13.5 5.5C14.0523 5.5 14.5 5.94772 14.5 6.5V8.5C14.5 9.05228 14.0523 9.5 13.5 9.5M1.5 5.5C0.947716 5.5 0.5 5.94772 0.5 6.5V8.5C0.5 9.05228 0.947716 9.5 1.5 9.5M13.5 9.5H1.5M13.5 9.5C14.0523 9.5 14.5 9.94772 14.5 10.5V12.5C14.5 13.0523 14.0523 13.5 13.5 13.5H1.5C0.947716 13.5 0.5 13.0523 0.5 12.5V10.5C0.5 9.94772 0.947716 9.5 1.5 9.5M2 3.5H5M2 7.5H5M2 11.5H5"
      stroke={color}
    />
  {:else}
    <path
      fill-rule="evenodd"
      clip-rule="evenodd"
      d="M0 2.5C0 1.67157 0.671573 1 1.5 1H13.5C14.3284 1 15 1.67157 15 2.5V4.5C15 4.88418 14.8556 5.23463 14.618 5.5C14.8556 5.76538 15 6.11582 15 6.5V8.5C15 8.88418 14.8556 9.23462 14.618 9.5C14.8556 9.76538 15 10.1158 15 10.5V12.5C15 13.3284 14.3284 14 13.5 14H1.5C0.671573 14 0 13.3284 0 12.5V10.5C0 10.1158 0.14443 9.76538 0.38195 9.5C0.144428 9.23462 0 8.88418 0 8.5V6.5C0 6.11582 0.144427 5.76538 0.381947 5.5C0.144427 5.23462 0 4.88418 0 4.5V2.5ZM2 4H5V3H2V4ZM5 8H2V7H5V8ZM2 12H5V11H2V12Z"
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
