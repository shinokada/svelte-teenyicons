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
  export let ariaLabel = 'bed double';
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
      d="M14.5 7V15M0.5 7V15M0 10.5H15M0 7.5H15M2 5.5H6M9 5.5H13M0.5 6V0.5H14.5V6"
      stroke={color}
    />
  {:else}
    <path d="M0 0H15V6H14V1H1V6H0V0Z" fill={color} /> <path d="M6 6H2V5H6V6Z" fill={color} />
    <path d="M0 15H1V11H14V15H15V7H0V15Z" fill={color} /> <path d="M9 6H13V5H9V6Z" fill={color} />
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
@prop export let ariaLabel = 'bed double';
-->
