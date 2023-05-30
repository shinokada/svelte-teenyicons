<script lang="ts">
  export let size: string = '15';
  export let color: string = 'black';
  export let variation: 'solid' | 'outline' = 'outline';
  export let ariaLabel = 'refresh alt';
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
      d="M0.5 7.5C0.5 3.63401 3.63401 0.5 7.5 0.5C9.73096 0.5 11.7182 1.54367 13 3.1694M14.5 7.5C14.5 11.366 11.366 14.5 7.5 14.5C5.26904 14.5 3.28183 13.4563 2 11.8306M5 11.5H1.5V15M13.5 0V3.5L10 3.5"
      stroke={color}
    />
  {:else}
    <path
      fill-rule="evenodd"
      clip-rule="evenodd"
      d="M7.5 1C3.91015 1 1 3.91015 1 7.5H0C0 3.35786 3.35786 0 7.5 0C9.6733 0 11.6308 0.924852 13 2.40095V0H14V4L10 4V3L12.1905 3C11.007 1.76671 9.34315 1 7.5 1ZM7.5 14C11.0899 14 14 11.0899 14 7.5H15C15 11.6421 11.6421 15 7.5 15C5.3267 15 3.36918 14.0751 2 12.599V15H1V11H5V12H2.80955C3.993 13.2333 5.65685 14 7.5 14Z"
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
