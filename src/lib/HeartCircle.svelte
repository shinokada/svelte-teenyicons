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
  export let ariaLabel = 'heart circle';
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
      d="M6.5 5.5L7.5 6.5L8.5 5.5C9.05228 4.94772 9.94772 4.94772 10.5 5.5C11.0523 6.05228 11.0523 6.94771 10.5 7.5L7.5 10.5L4.5 7.5C3.94772 6.94772 3.94772 6.05228 4.5 5.5C5.05228 4.94772 5.94771 4.94771 6.5 5.5Z"
      stroke={color}
    />
    <path
      d="M0.5 7.5C0.5 11.366 3.63401 14.5 7.5 14.5C11.366 14.5 14.5 11.366 14.5 7.5C14.5 3.63401 11.366 0.5 7.5 0.5C3.63401 0.5 0.5 3.63401 0.5 7.5Z"
      stroke={color}
    />
  {:else}
    <path
      fill-rule="evenodd"
      clip-rule="evenodd"
      d="M0 7.5C0 3.35786 3.35786 0 7.5 0C11.6421 0 15 3.35786 15 7.5C15 11.6421 11.6421 15 7.5 15C3.35786 15 0 11.6421 0 7.5ZM4.14635 5.14648C4.8939 4.39893 6.10591 4.39893 6.85346 5.14648L7.49991 5.79292L8.14635 5.14648C8.8939 4.39893 10.1059 4.39893 10.8535 5.14648C11.601 5.89402 11.601 7.10603 10.8535 7.85358L7.49991 11.2071L4.14635 7.85358C3.39881 7.10604 3.39881 5.89402 4.14635 5.14648Z"
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
@prop export let ariaLabel = 'heart circle';
-->
