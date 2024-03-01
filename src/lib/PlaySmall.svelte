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
  export let ariaLabel = 'play small';
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
    <path d="M6.5 9.5V5.5L10 7.5L6.5 9.5Z" stroke={color} stroke-linejoin="round" />
  {:else}
    <path
      d="M6.74807 5.06588C6.59332 4.97745 6.40319 4.97808 6.24904 5.06754C6.09488 5.15701 6 5.32176 6 5.5V9.5C6 9.67824 6.09488 9.84299 6.24904 9.93246C6.40319 10.0219 6.59332 10.0226 6.74807 9.93412L10.2481 7.93412C10.4039 7.8451 10.5 7.67943 10.5 7.5C10.5 7.32057 10.4039 7.1549 10.2481 7.06588L6.74807 5.06588Z"
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
@prop export let ariaLabel = 'play small';
-->
