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
  export let ariaLabel = 'forward small';
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
    <path d="M8.5 9.5V5.5L12 7.5L8.5 9.5Z" stroke={color} stroke-linejoin="round" />
    <path d="M4.5 9.5V5.5L8 7.5L4.5 9.5Z" stroke={color} stroke-linejoin="round" />
  {:else}
    <path
      d="M4.74807 5.06588C4.59332 4.97745 4.40319 4.97808 4.24904 5.06754C4.09488 5.15701 4 5.32176 4 5.5V9.5C4 9.67824 4.09488 9.84299 4.24904 9.93246C4.40319 10.0219 4.59332 10.0226 4.74807 9.93412L8 8.07588V9.5C8 9.67824 8.09488 9.84299 8.24904 9.93246C8.40319 10.0219 8.59332 10.0226 8.74807 9.93412L12.2481 7.93412C12.4039 7.8451 12.5 7.67943 12.5 7.5C12.5 7.32057 12.4039 7.1549 12.2481 7.06588L8.74807 5.06588C8.59332 4.97745 8.40319 4.97808 8.24904 5.06754C8.09488 5.15701 8 5.32176 8 5.5V6.92412L4.74807 5.06588Z"
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
@prop export let ariaLabel = 'forward small';
-->
