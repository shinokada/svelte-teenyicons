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
  export let ariaLabel = 'cart minus';
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
      d="M0.5 0.5L1.1 2.5M1.1 2.5L3.5 10.5H14.5V4.5C14.5 3.39543 13.6046 2.5 12.5 2.5H1.1ZM6 6.5H11M12.5 14.5C11.9477 14.5 11.5 14.0523 11.5 13.5C11.5 12.9477 11.9477 12.5 12.5 12.5C13.0523 12.5 13.5 12.9477 13.5 13.5C13.5 14.0523 13.0523 14.5 12.5 14.5ZM4.5 13.5C4.5 12.9477 4.94772 12.5 5.5 12.5C6.05228 12.5 6.5 12.9477 6.5 13.5C6.5 14.0523 6.05228 14.5 5.5 14.5C4.94772 14.5 4.5 14.0523 4.5 13.5Z"
      stroke={color}
    />
  {:else}
    <path
      fill-rule="evenodd"
      clip-rule="evenodd"
      d="M0.0209961 0.643671L0.978822 0.356323L1.47192 2H12.4999C13.8806 2 14.9999 3.11929 14.9999 4.5V11H3.12789L0.0209961 0.643671ZM6 7H11V6H6V7Z"
      fill={color}
    />
    <path
      fill-rule="evenodd"
      clip-rule="evenodd"
      d="M4 13.5C4 12.6716 4.67157 12 5.5 12C6.32843 12 7 12.6716 7 13.5C7 14.3284 6.32843 15 5.5 15C4.67157 15 4 14.3284 4 13.5ZM5.5 13C5.22386 13 5 13.2239 5 13.5C5 13.7761 5.22386 14 5.5 14C5.77614 14 6 13.7761 6 13.5C6 13.2239 5.77614 13 5.5 13Z"
      fill={color}
    />
    <path
      fill-rule="evenodd"
      clip-rule="evenodd"
      d="M11 13.5C11 12.6716 11.6716 12 12.5 12C13.3284 12 14 12.6716 14 13.5C14 14.3284 13.3284 15 12.5 15C11.6716 15 11 14.3284 11 13.5ZM12.5 13C12.2239 13 12 13.2239 12 13.5C12 13.7761 12.2239 14 12.5 14C12.7761 14 13 13.7761 13 13.5C13 13.2239 12.7761 13 12.5 13Z"
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
@prop export let ariaLabel = 'cart minus';
-->
