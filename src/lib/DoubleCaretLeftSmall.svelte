<script lang="ts">
  export let size: string = '15';
  export let role: string = 'img';
  export let color: string = 'currentColor';
  export let variation: 'solid' | 'outline' = 'outline';
  export let ariaLabel = 'double caret left small';
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
      d="M6.5 9.5L4.5 7.5L6.5 5.5M9.5 9.5L7.5 7.5L9.5 5.5"
      stroke={color}
      stroke-linecap="square"
    />
  {:else}
    <path
      fill-rule="evenodd"
      clip-rule="evenodd"
      d="M7.20712 5.50001L5.20712 7.50001L7.20712 9.50001L6.50001 10.2071L3.79291 7.50001L6.50001 4.79291L7.20712 5.50001ZM10.2071 5.50001L8.20712 7.50001L10.2071 9.50001L9.50001 10.2071L6.79291 7.50001L9.50001 4.79291L10.2071 5.50001Z"
      fill={color}
    />
  {/if}
</svg>

<!--
@component
[Go to docs](https://svelte-teenyicons.vercel.app/)
## Props
@prop export let size: string = '15';
@prop export let role: string = 'img';
@prop export let color: string = 'currentColor';
@prop export let variation: 'solid' | 'outline' = 'outline';
@prop export let ariaLabel = 'double caret left small';
-->
