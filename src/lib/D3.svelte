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
  export let ariaLabel = 'd3';
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
      d="M0 1.5H1.5C4.81371 1.5 7.5 4.18629 7.5 7.5C7.5 10.8137 4.81371 13.5 1.5 13.5H0M7 1.5H11.5C13.1569 1.5 14.5 2.84315 14.5 4.5C14.5 6.15685 13.1569 7.5 11.5 7.5M11.5 7.5H9M11.5 7.5H9.5M11.5 7.5C13.1569 7.5 14.5 8.84315 14.5 10.5C14.5 12.1569 13.1569 13.5 11.5 13.5H7"
      stroke={color}
    />
  {:else}
    <path
      fill-rule="evenodd"
      clip-rule="evenodd"
      d="M1.5 2H0V1H1.5C5.08985 1 8 3.91015 8 7.5C8 11.0899 5.08985 14 1.5 14H0V13H1.5C4.53757 13 7 10.5376 7 7.5C7 4.46243 4.53757 2 1.5 2ZM11.5 2H7V1H11.5C13.433 1 15 2.567 15 4.5C15 5.77316 14.3202 6.88755 13.3038 7.5C14.3202 8.11245 15 9.22684 15 10.5C15 12.433 13.433 14 11.5 14H7V13H11.5C12.8807 13 14 11.8807 14 10.5C14 9.11929 12.8807 8 11.5 8H9V7H11.5C12.8807 7 14 5.88071 14 4.5C14 3.11929 12.8807 2 11.5 2Z"
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
@prop export let ariaLabel = 'd3';
-->
