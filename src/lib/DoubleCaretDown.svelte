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
  export let ariaLabel = 'double caret down';
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
    <path d="M1 7L7.5 14L14 7M1 1.5L7.5 8.5L14 1.5" stroke={color} stroke-linecap="square" />
  {:else}
    <path
      fill-rule="evenodd"
      clip-rule="evenodd"
      d="M14.7066 1.47385L7.5 9.23483L0.293375 1.47385L1.02617 0.793396L7.5 7.76521L13.9738 0.793396L14.7066 1.47385ZM1.02617 6.2934L7.5 13.2652L13.9738 6.2934L14.7066 6.97385L7.5 14.7348L0.293375 6.97385L1.02617 6.2934Z"
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
@prop export let ariaLabel = 'double caret down';
-->
