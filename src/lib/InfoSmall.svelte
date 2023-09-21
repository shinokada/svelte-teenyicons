<script lang="ts">
  export let size: string = '15';
  export let role: string = 'img';
  export let color: string = 'currentColor';
  export let variation: 'solid' | 'outline' = 'outline';
  export let ariaLabel = 'info small';
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
      d="M7 4.49999V4.99999H8V4.49999H7ZM8 4.48999V3.98999H7V4.48999H8ZM8 11L8 6.99999H7L7 11H8ZM8 4.49999V4.48999H7V4.49999H8ZM6 7.99999H7.5V6.99999H6V7.99999ZM6 11H9V9.99999H6V11Z"
      fill={color}
    />
  {:else}
    <path
      fill-rule="evenodd"
      clip-rule="evenodd"
      d="M8 3.98999V4.99999H7V3.98999H8ZM6 11V9.99999H7L7 7.99999H6V6.99999L8 6.99999L8 9.99999H9V11H6Z"
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
@prop export let ariaLabel = 'info small';
-->
