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
  export let ariaLabel = 'rewind small';
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
    <path d="M6.5 9.5V5.5L3 7.5L6.5 9.5Z" stroke={color} stroke-linejoin="round" />
    <path d="M10.5 9.5V5.5L7 7.5L10.5 9.5Z" stroke={color} stroke-linejoin="round" />
  {:else}
    <path
      d="M7 5.5C7 5.32176 6.90512 5.15701 6.75096 5.06754C6.59681 4.97808 6.40668 4.97745 6.25193 5.06588L2.75193 7.06588C2.59614 7.1549 2.5 7.32057 2.5 7.5C2.5 7.67943 2.59614 7.8451 2.75193 7.93412L6.25193 9.93412C6.40668 10.0226 6.59681 10.0219 6.75096 9.93246C6.90512 9.84299 7 9.67824 7 9.5V8.07588L10.2519 9.93412C10.4067 10.0226 10.5968 10.0219 10.751 9.93246C10.9051 9.84299 11 9.67824 11 9.5V5.5C11 5.32176 10.9051 5.15701 10.751 5.06754C10.5968 4.97808 10.4067 4.97745 10.2519 5.06588L7 6.92412V5.5Z"
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
@prop export let ariaLabel = 'rewind small';
-->
