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
  export let ariaLabel = 'wifi full';
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
      d="M3.21904 9.31822C4.37368 7.91859 5.91674 7.15689 7.50001 7.15689V6.15689C5.5826 6.15689 3.76836 7.08091 2.44765 8.68186L3.21904 9.31822ZM7.50001 7.15689C9.08328 7.15689 10.6263 7.91859 11.781 9.31822L12.5524 8.68186C11.2317 7.08091 9.41742 6.15689 7.50001 6.15689V7.15689ZM0.885695 6.31819C2.65917 4.16841 5.04156 2.98529 7.5 2.98529V1.98529C4.70742 1.98529 2.05386 3.33073 0.114305 5.68183L0.885695 6.31819ZM7.5 2.98529C9.95844 2.98529 12.3408 4.16841 14.1143 6.31819L14.8857 5.68183C12.9461 3.33073 10.2926 1.98529 7.5 1.98529V2.98529ZM7.5 12C7.22386 12 7 11.7762 7 11.5H6C6 12.3284 6.67157 13 7.5 13V12ZM8 11.5C8 11.7762 7.77614 12 7.5 12V13C8.32843 13 9 12.3284 9 11.5H8ZM7.5 11C7.77614 11 8 11.2239 8 11.5H9C9 10.6716 8.32843 10 7.5 10V11ZM7.5 10C6.67157 10 6 10.6716 6 11.5H7C7 11.2239 7.22386 11 7.5 11V10Z"
      fill={color}
    />
  {:else}
    <path
      d="M7.49995 2.98529C5.04151 2.98529 2.65912 4.16841 0.885647 6.31819L0.114258 5.68183C2.05381 3.33073 4.70738 1.98529 7.49995 1.98529C10.2925 1.98529 12.9461 3.33073 14.8856 5.68183L14.1143 6.31819C12.3408 4.16841 9.9584 2.98529 7.49995 2.98529Z"
      fill={color}
    />
    <path
      d="M7.50012 7.15689C5.91684 7.15689 4.37378 7.91859 3.21914 9.31822L2.44775 8.68186C3.76847 7.08091 5.58271 6.15689 7.50012 6.15689C9.41752 6.15689 11.2318 7.08091 12.5525 8.68186L11.7811 9.31822C10.6264 7.91859 9.08339 7.15689 7.50012 7.15689Z"
      fill={color}
    />
    <path
      d="M6 11.5C6 10.6716 6.67157 10 7.5 10C8.32843 10 9 10.6716 9 11.5C9 12.3284 8.32843 13 7.5 13C6.67157 13 6 12.3284 6 11.5Z"
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
@prop export let ariaLabel = 'wifi full';
-->
