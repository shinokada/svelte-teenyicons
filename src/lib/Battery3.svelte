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
  export let ariaLabel = 'battery 3';
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
      d="M14.5 10L14.5 5M2.5 11L2.5 4M4.5 11V4M6.5 11V4M12.5 11.5V3.5C12.5 2.94772 12.0523 2.5 11.5 2.5L1.5 2.5C0.947715 2.5 0.5 2.94772 0.5 3.5L0.5 11.5C0.5 12.0523 0.947715 12.5 1.5 12.5H11.5C12.0523 12.5 12.5 12.0523 12.5 11.5Z"
      stroke={color}
    />
  {:else}
    <path
      fill-rule="evenodd"
      clip-rule="evenodd"
      d="M0 11.5C0 12.3284 0.671573 13 1.5 13L11.5 13C12.3284 13 13 12.3284 13 11.5V3.5C13 2.67157 12.3284 2 11.5 2H1.5C0.671572 2 0 2.67157 0 3.5V11.5ZM3 11V4H2V11H3ZM5 11V4H4V11H5ZM7 4V11H6V4H7Z"
      fill={color}
    /> <path d="M15 5V10H14V5H15Z" fill={color} />
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
@prop export let ariaLabel = 'battery 3';
-->
