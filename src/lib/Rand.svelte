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
  export let ariaLabel = 'rand';
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
      d="M3.5 14V8.5M3.5 8.5V1.5H8C9.933 1.5 11.5 3.067 11.5 5C11.5 6.933 9.933 8.5 8 8.5H3.5ZM3.5 8.5H8.5C10.1569 8.5 11.5 9.84315 11.5 11.5V14"
      stroke={color}
    />
  {:else}
    <path
      fill-rule="evenodd"
      clip-rule="evenodd"
      d="M3 1H8C10.2091 1 12 2.79086 12 5C12 6.43196 11.2475 7.68818 10.1165 8.39483C11.2358 8.97873 12 10.1501 12 11.5V14H11V11.5C11 10.1193 9.88071 9 8.5 9H4V14H3V1ZM4 8H8C9.65685 8 11 6.65685 11 5C11 3.34315 9.65685 2 8 2H4V8Z"
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
@prop export let ariaLabel = 'rand';
-->
