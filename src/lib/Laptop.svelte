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
  export let ariaLabel = 'laptop';
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
      d="M0 13.5H15M1.5 2.5L1.5 10.5C1.5 11.0523 1.94771 11.5 2.5 11.5H12.5C13.0523 11.5 13.5 11.0523 13.5 10.5V2.5C13.5 1.94772 13.0523 1.5 12.5 1.5L2.5 1.5C1.94772 1.5 1.5 1.94772 1.5 2.5Z"
      stroke={color}
    />
  {:else}
    <path
      d="M2.5 1C1.67157 1 1 1.67157 1 2.5L1 10.5C1 11.3284 1.67157 12 2.5 12H12.5C13.3284 12 14 11.3284 14 10.5V2.5C14 1.67157 13.3284 1 12.5 1H2.5Z"
      fill={color}
    /> <path d="M0 14H15V13H0V14Z" fill={color} />
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
@prop export let ariaLabel = 'laptop';
-->
