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
  export let ariaLabel = 'direction';
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
    <path d="M0.5 0.5L6.5 14.5L8.5 8.5L14.5 6.5L0.5 0.5Z" stroke={color} stroke-linejoin="round" />
  {:else}
    <path
      d="M0.696974 0.0404421C0.509053 -0.0400956 0.291031 0.00189163 0.146461 0.146461C0.00189163 0.291031 -0.0400956 0.509053 0.0404421 0.696974L6.04044 14.697C6.12222 14.8878 6.31338 15.0082 6.52079 14.9996C6.7282 14.991 6.90871 14.8551 6.97436 14.6581L8.8953 8.8953L14.6581 6.97436C14.8551 6.90871 14.991 6.7282 14.9996 6.52079C15.0082 6.31338 14.8878 6.12222 14.697 6.04044L0.696974 0.0404421Z"
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
@prop export let ariaLabel = 'direction';
-->
