<script lang="ts">
  export let size: string = '15';
  export let role: string = 'img';
  export let color: string = 'currentColor';
  export let variation: 'solid' | 'outline' = 'outline';
  export let ariaLabel = 'arrow down';
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
    <path d="M7.5 13.5L11.5 9.5M7.5 13.5L3.5 9.5M7.5 13.5V1" stroke={color} />
  {:else}
    <path
      fill-rule="evenodd"
      clip-rule="evenodd"
      d="M8.00001 1V12.2929L11.1465 9.14645L11.8536 9.85355L7.50001 14.2071L3.14645 9.85355L3.85356 9.14645L7.00001 12.2929V1H8.00001Z"
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
@prop export let ariaLabel = 'arrow down';
-->
