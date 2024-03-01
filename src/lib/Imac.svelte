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
  export let ariaLabel = 'imac';
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
      d="M2 14.5H13M7.5 10.5V14.5M0 7.5H15M0.5 1.5L0.5 9.5C0.5 10.0523 0.947715 10.5 1.5 10.5L13.5 10.5C14.0523 10.5 14.5 10.0523 14.5 9.5V1.5C14.5 0.947716 14.0523 0.500001 13.5 0.500001L1.5 0.5C0.947715 0.5 0.5 0.947716 0.5 1.5Z"
      stroke={color}
    />
  {:else}
    <path
      d="M13.5 0C14.3284 0 15 0.671573 15 1.5V7H0V1.5C0 0.671573 0.671573 0 1.5 0H13.5Z"
      fill={color}
    />
    <path
      d="M0 8V9.5C0 10.3284 0.671573 11 1.5 11H7V14H2V15H13V14H8V11H13.5C14.3284 11 15 10.3284 15 9.5V8H0Z"
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
@prop export let ariaLabel = 'imac';
-->
