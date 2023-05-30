<script lang="ts">
  export let size: string = '15';
  export let color: string = 'black';
  export let variation: 'solid' | 'outline' = 'outline';
  export let ariaLabel = 'briefcase';
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
      d="M5.5 3V2.5C5.5 1.39543 6.39543 0.5 7.5 0.5C8.60457 0.5 9.5 1.39543 9.5 2.5V3M0.5 11.5H14.5M1.5 3.5H13.5C14.0523 3.5 14.5 3.94772 14.5 4.5V13.5C14.5 14.0523 14.0523 14.5 13.5 14.5H1.5C0.947716 14.5 0.5 14.0523 0.5 13.5V4.5C0.5 3.94772 0.947715 3.5 1.5 3.5Z"
      stroke={color}
    />
  {:else}
    <path
      fill-rule="evenodd"
      clip-rule="evenodd"
      d="M5 2.5V3H1.5C0.671573 3 0 3.67157 0 4.5V11H15V4.5C15 3.67157 14.3284 3 13.5 3H10V2.5C10 1.11929 8.88071 0 7.5 0C6.11929 0 5 1.11929 5 2.5ZM7.5 1C6.67157 1 6 1.67157 6 2.5V3H9V2.5C9 1.67157 8.32843 1 7.5 1Z"
      fill={color}
    />
    <path
      d="M15 12H0V13.5C0 14.3284 0.671573 15 1.5 15H13.5C14.3284 15 15 14.3284 15 13.5V12Z"
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
