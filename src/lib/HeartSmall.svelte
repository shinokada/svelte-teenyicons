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
  export let ariaLabel = 'heart small';
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
      d="M6.50003 5.50003L7.50003 6.50003L8.50003 5.50003C9.05231 4.94774 9.94774 4.94774 10.5 5.50003C11.0523 6.05231 11.0523 6.94774 10.5 7.50003L7.50003 10.5L4.50003 7.50003C3.94774 6.94774 3.94774 6.05231 4.50003 5.50003C5.05231 4.94774 5.94774 4.94774 6.50003 5.50003Z"
      stroke={color}
    />
  {:else}
    <path
      d="M6.76507 5.23486C6.06634 4.53613 4.93347 4.53613 4.23474 5.23486C3.53601 5.9336 3.53601 7.06646 4.23474 7.7652L7.49991 11.0304L10.7651 7.76519C11.4638 7.06646 11.4638 5.9336 10.7651 5.23486C10.0663 4.53613 8.93347 4.53613 8.23474 5.23486L7.49991 5.9697L6.76507 5.23486Z"
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
@prop export let ariaLabel = 'heart small';
-->
