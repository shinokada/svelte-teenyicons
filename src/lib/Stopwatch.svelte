<script lang="ts">
  interface CtxType {
    size?: string;
    role?: string;
    color?: string;
    variation?: 'solid' | 'outline';
  }

  import { getContext } from 'svelte';
  const ctx: CtxType = getContext('iconCtx') ?? {};
  export let size: string = ctx.size || '15';
  export let role: string = ctx.role || 'img';
  export let color: string = ctx.color || 'currentColor';
  export let variation: 'solid' | 'outline' = 'outline';
  export let ariaLabel = 'stopwatch';
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
      d="M7.5 5V8.5H10M6 0.5H9M7.5 2.5C4.18629 2.5 1.5 5.18629 1.5 8.5C1.5 11.8137 4.18629 14.5 7.5 14.5C10.8137 14.5 13.5 11.8137 13.5 8.5C13.5 5.18629 10.8137 2.5 7.5 2.5Z"
      stroke={color}
    />
  {:else}
    <path d="M9 1H6V0H9V1Z" fill={color} />
    <path
      fill-rule="evenodd"
      clip-rule="evenodd"
      d="M7.5 2C3.91015 2 1 4.91015 1 8.5C1 12.0899 3.91015 15 7.5 15C11.0899 15 14 12.0899 14 8.5C14 4.91015 11.0899 2 7.5 2ZM8 8V5H7V9H10V8H8Z"
      fill={color}
    />
  {/if}
</svg>

<!--
@component
[Go to docs](https://svelte-teenyicons.codewithshin.com/)
## Props
@prop export let size: string = ctx.size || '15';
@prop export let role: string = ctx.role || 'img';
@prop export let color: string = ctx.color || 'currentColor';
@prop export let variation: 'solid' | 'outline' = 'outline';
@prop export let ariaLabel = 'stopwatch';
-->
