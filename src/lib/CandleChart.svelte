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
  export let ariaLabel = 'candle chart';
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
      d="M0.5 0V14.5H15M8.5 0V3.5M3.5 9.5V12M3.5 4V5.5M13.5 4V6.5M13.5 10.5V13M2.5 5.5H4.5V9.5H2.5V5.5ZM7.5 3.5H9.5V7.5H7.5V3.5ZM12.5 6.5H14.5V10.5H12.5V6.5Z"
      stroke={color}
    />
  {:else}
    <path d="M1 0H0V15H15V14H1V0Z" fill={color} /> <path d="M8 0V3H7V8H10V3H9V0H8Z" fill={color} />
    <path d="M3 4V5H2V10H3V12H4V10H5V5H4V4H3Z" fill={color} />
    <path d="M12 6H13V4H14V6H15V11H14V13H13V11H12V6Z" fill={color} />
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
@prop export let ariaLabel = 'candle chart';
-->
