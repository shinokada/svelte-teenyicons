<script lang="ts">
  export let size: string = '15';
  export let color: string = 'black';
  export let variation: 'solid' | 'outline' = 'outline';
  export let ariaLabel = 'star small';
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
      d="M7.5 9.80416L5.33677 11L5.75 8.46718L4 6.6736L6.41839 6.30434L7.5 4L8.58161 6.30434L11 6.6736L9.25 8.46718L9.66323 11L7.5 9.80416Z"
      stroke={color}
      stroke-linecap="round"
      stroke-linejoin="round"
    />
  {:else}
    <path
      d="M7.95263 3.78755C7.87026 3.61206 7.69387 3.5 7.50001 3.5C7.30615 3.5 7.12976 3.61206 7.04739 3.78755L6.07916 5.85035L3.92454 6.17933C3.73928 6.20761 3.58539 6.33713 3.52588 6.51485C3.46638 6.69257 3.51126 6.88864 3.64214 7.02278L5.2159 8.63573L4.84331 10.9195C4.81248 11.1085 4.89228 11.2985 5.04881 11.4087C5.20534 11.519 5.41111 11.5302 5.57868 11.4376L7.50001 10.3755L9.42134 11.4376C9.58892 11.5302 9.79468 11.519 9.95122 11.4087C10.1077 11.2985 10.1875 11.1085 10.1567 10.9195L9.78412 8.63573L11.3579 7.02278C11.4888 6.88864 11.5336 6.69257 11.4741 6.51485C11.4146 6.33713 11.2607 6.20761 11.0755 6.17933L8.92087 5.85035L7.95263 3.78755Z"
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
