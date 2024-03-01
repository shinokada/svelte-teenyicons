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
  export let ariaLabel = 'scan';
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
      d="M0.5 5V2.5C0.5 1.39543 1.39543 0.5 2.5 0.5H5M10 0.5H12.5C13.6046 0.5 14.5 1.39543 14.5 2.5V5M0.5 10V12.5C0.5 13.6046 1.39543 14.5 2.5 14.5H5M14.5 10V12.5C14.5 13.6046 13.6046 14.5 12.5 14.5H10M2 7.5H13"
      stroke={color}
    />
  {:else}
    <path
      fill-rule="evenodd"
      clip-rule="evenodd"
      d="M2.5 1C1.67157 1 1 1.67157 1 2.5V5H0V2.5C0 1.11929 1.11929 0 2.5 0H5V1H2.5ZM12.5 1H10V0H12.5C13.8807 0 15 1.11929 15 2.5V5H14V2.5C14 1.67157 13.3284 1 12.5 1ZM13 8H2V7H13V8ZM0 12.5V10H1V12.5C1 13.3284 1.67157 14 2.5 14H5V15H2.5C1.11929 15 0 13.8807 0 12.5ZM14 12.5V10H15V12.5C15 13.8807 13.8807 15 12.5 15H10V14H12.5C13.3284 14 14 13.3284 14 12.5Z"
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
@prop export let ariaLabel = 'scan';
-->
