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
  export let ariaLabel = 'pool';
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
      d="M1 12.6C1.65 13.3333 2.65455 14 3.95455 14C6.90909 14 7.5 12 10.4545 12C11.8136 12 13.0545 12.7333 14 13.4667M2.5 12V3.72724C2.5 1.94542 3.85458 0.5 5.63639 0.5M9.5 10V3.63639C9.5 1.85458 10.9 0.5 12.6818 0.5M2.5 4.5H9.5M2.5 8.5H9.5"
      stroke={color}
      stroke-miterlimit="10"
      stroke-linejoin="round"
    />
  {:else}
    <path
      fill-rule="evenodd"
      clip-rule="evenodd"
      d="M5.63639 1C4.14922 1 3 2.20269 3 3.72724V4H9V3.63639C9 1.56904 10.6333 0 12.6818 0V1C11.1667 1 10 2.14011 10 3.63639V10H9V9H3V12H2V3.72724C2 1.68816 3.55993 0 5.63639 0V1ZM3 8H9V5H3V8Z"
      fill={color}
    />
    <path
      d="M7.43931 13.4416C6.54499 13.9461 5.56317 14.5 3.95454 14.5C2.47163 14.5 1.34063 13.7381 0.625824 12.9317L1.37417 12.2683C1.95937 12.9286 2.83745 13.5 3.95454 13.5C5.29393 13.5 6.0834 13.0584 6.95888 12.5645L6.96977 12.5584C7.8641 12.0539 8.84591 11.5 10.4545 11.5C11.9851 11.5 13.3377 12.3202 14.3064 13.0716L13.6936 13.8618C12.7714 13.1465 11.6421 12.5 10.4545 12.5C9.11516 12.5 8.32568 12.9416 7.4502 13.4355L7.43931 13.4416Z"
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
@prop export let ariaLabel = 'pool';
-->
