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
  export let ariaLabel = 'more vertical';
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
      d="M7.5 3C7.22386 3 7 2.77614 7 2.5C7 2.22386 7.22386 2 7.5 2C7.77614 2 8 2.22386 8 2.5C8 2.77614 7.77614 3 7.5 3Z"
      stroke={color}
    />
    <path
      d="M7.5 8C7.22386 8 7 7.77614 7 7.5C7 7.22386 7.22386 7 7.5 7C7.77614 7 8 7.22386 8 7.5C8 7.77614 7.77614 8 7.5 8Z"
      stroke={color}
    />
    <path
      d="M7.5 13C7.22386 13 7 12.7761 7 12.5C7 12.2239 7.22386 12 7.5 12C7.77614 12 8 12.2239 8 12.5C8 12.7761 7.77614 13 7.5 13Z"
      stroke={color}
    />
  {:else}
    <path
      fill-rule="evenodd"
      clip-rule="evenodd"
      d="M6.49999 2.5C6.49999 1.94772 6.9477 1.5 7.49999 1.5C8.05227 1.5 8.49999 1.94772 8.49999 2.5C8.49999 3.05228 8.05227 3.5 7.49999 3.5C6.9477 3.5 6.49999 3.05228 6.49999 2.5ZM6.49998 7.5C6.49998 6.94772 6.9477 6.5 7.49998 6.5C8.05227 6.5 8.49998 6.94772 8.49998 7.5C8.49998 8.05228 8.05227 8.5 7.49998 8.5C6.9477 8.5 6.49998 8.05228 6.49998 7.5ZM6.49998 12.5C6.49998 11.9477 6.9477 11.5 7.49998 11.5C8.05227 11.5 8.49998 11.9477 8.49998 12.5C8.49998 13.0523 8.05227 13.5 7.49998 13.5C6.9477 13.5 6.49998 13.0523 6.49998 12.5Z"
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
@prop export let ariaLabel = 'more vertical';
-->
