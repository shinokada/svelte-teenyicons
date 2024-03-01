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
  export let ariaLabel = 'nes';
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
      d="M3.5 7V10M2 8.5H5M11 9.5H12M9 9.5H10M1.5 3.5H13.5C14.0523 3.5 14.5 3.94772 14.5 4.5V10.5C14.5 11.0523 14.0523 11.5 13.5 11.5H1.5C0.947716 11.5 0.5 11.0523 0.5 10.5V4.5C0.5 3.94772 0.947715 3.5 1.5 3.5Z"
      stroke={color}
    />
  {:else}
    <path
      fill-rule="evenodd"
      clip-rule="evenodd"
      d="M0 4.5C0 3.67157 0.671573 3 1.5 3H13.5C14.3284 3 15 3.67157 15 4.5V10.5C15 11.3284 14.3284 12 13.5 12H1.5C0.671573 12 0 11.3284 0 10.5V4.5ZM3 10V9H2V8H3V7H4V8H5V9H4V10H3ZM11 10H12V9H11V10ZM10 10H9V9H10V10Z"
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
@prop export let ariaLabel = 'nes';
-->
