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
  export let ariaLabel = 'lego';
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
      d="M3.5 3H11.5V2H3.5V3ZM13 4.5V12.5H14V4.5H13ZM11.5 14H3.5V15H11.5V14ZM2 12.5V4.5H1V12.5H2ZM3.5 14C2.67157 14 2 13.3284 2 12.5H1C1 13.8807 2.11929 15 3.5 15V14ZM13 12.5C13 13.3284 12.3284 14 11.5 14V15C12.8807 15 14 13.8807 14 12.5H13ZM11.5 3C12.3284 3 13 3.67157 13 4.5H14C14 3.11929 12.8807 2 11.5 2V3ZM3.5 2C2.11929 2 1 3.11929 1 4.5H2C2 3.67157 2.67157 3 3.5 3V2ZM5 8H6V7H5V8ZM9 8H10V7H9V8ZM10.1 9.7C8.8 11.4333 6.2 11.4333 4.9 9.7L4.1 10.3C5.8 12.5667 9.2 12.5667 10.9 10.3L10.1 9.7ZM5 2.5V1.5H4V2.5H5ZM5.5 1H9.5V0H5.5V1ZM10 1.5V2.5H11V1.5H10ZM9.5 1C9.77614 1 10 1.22386 10 1.5H11C11 0.671573 10.3284 0 9.5 0V1ZM5 1.5C5 1.22386 5.22386 1 5.5 1V0C4.67157 0 4 0.671573 4 1.5H5Z"
      fill={color}
    />
  {:else}
    <path
      fill-rule="evenodd"
      clip-rule="evenodd"
      d="M4 1.5C4 0.671573 4.67157 0 5.5 0H9.5C10.3284 0 11 0.671573 11 1.5V2H11.5C12.8807 2 14 3.11929 14 4.5V12.5C14 13.8807 12.8807 15 11.5 15H3.5C2.11929 15 1 13.8807 1 12.5V4.5C1 3.11929 2.11929 2 3.5 2H4V1.5ZM5 7V8H6V7H5ZM9 7V8H10V7H9ZM4.9001 9.7C6.2001 11.4333 8.8001 11.4333 10.1001 9.7L10.9001 10.3C9.2001 12.5667 5.8001 12.5667 4.1001 10.3L4.9001 9.7Z"
      fill={color}
    />
  {/if}
</svg>

<!--
@component
[Go to docs](https://svelte-teenyicons.vercel.app/)
## Props
@prop export let size: string = ctx.size || '15';
@prop export let role: string = ctx.role || 'img';
@prop export let color: string = ctx.color || 'currentColor';
@prop export let variation: 'solid' | 'outline' = 'outline';
@prop export let ariaLabel = 'lego';
-->
