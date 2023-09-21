<script lang="ts">
  export let size: string = '15';
  export let role: string = 'img';
  export let color: string = 'currentColor';
  export let variation: 'solid' | 'outline' = 'outline';
  export let ariaLabel = 'double caret right small';
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
      d="M8.5 9.5L10.5 7.5L8.5 5.5M5.5 9.5L7.5 7.5L5.5 5.5"
      stroke={color}
      stroke-linecap="square"
    />
  {:else}
    <path
      fill-rule="evenodd"
      clip-rule="evenodd"
      d="M5.50001 4.79291L8.20712 7.50001L5.50001 10.2071L4.79291 9.50001L6.79291 7.50001L4.79291 5.50001L5.50001 4.79291ZM8.50001 4.79291L11.2071 7.50001L8.50001 10.2071L7.79291 9.50001L9.79291 7.50001L7.79291 5.50001L8.50001 4.79291Z"
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
@prop export let ariaLabel = 'double caret right small';
-->
