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
  export let ariaLabel = 'double caret left circle';
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
      d="M6.14645 9.85355L6.5 10.2071L7.20711 9.5L6.85355 9.14645L6.14645 9.85355ZM4.5 7.5L4.14645 7.14645L3.79289 7.5L4.14645 7.85355L4.5 7.5ZM6.85355 5.85355L7.20711 5.5L6.5 4.79289L6.14645 5.14645L6.85355 5.85355ZM9.14645 9.85355L9.5 10.2071L10.2071 9.5L9.85355 9.14645L9.14645 9.85355ZM7.5 7.5L7.14645 7.14645L6.79289 7.5L7.14645 7.85355L7.5 7.5ZM9.85355 5.85355L10.2071 5.5L9.5 4.79289L9.14645 5.14645L9.85355 5.85355ZM6.85355 9.14645L4.85355 7.14645L4.14645 7.85355L6.14645 9.85355L6.85355 9.14645ZM4.85355 7.85355L6.85355 5.85355L6.14645 5.14645L4.14645 7.14645L4.85355 7.85355ZM9.85355 9.14645L7.85355 7.14645L7.14645 7.85355L9.14645 9.85355L9.85355 9.14645ZM7.85355 7.85355L9.85355 5.85355L9.14645 5.14645L7.14645 7.14645L7.85355 7.85355ZM7.5 15C11.6421 15 15 11.6421 15 7.5H14C14 11.0899 11.0899 14 7.5 14V15ZM0 7.5C0 11.6421 3.35786 15 7.5 15V14C3.91015 14 1 11.0899 1 7.5H0ZM7.5 0C3.35786 0 0 3.35786 0 7.5H1C1 3.91015 3.91015 1 7.5 1V0ZM7.5 1C11.0899 1 14 3.91015 14 7.5H15C15 3.35786 11.6421 0 7.5 0V1Z"
      fill={color}
    />
  {:else}
    <path
      fill-rule="evenodd"
      clip-rule="evenodd"
      d="M15 7.5C15 3.35786 11.6421 0 7.5 0C3.35786 0 0 3.35786 0 7.5C0 11.6421 3.35786 15 7.5 15C11.6421 15 15 11.6421 15 7.5ZM9.49992 4.79285L6.79282 7.49995L9.49992 10.2071L10.207 9.49995L8.20703 7.49995L10.207 5.49995L9.49992 4.79285ZM6.49992 4.79285L3.79282 7.49995L6.49992 10.2071L7.20703 9.49995L5.20703 7.49995L7.20703 5.49995L6.49992 4.79285Z"
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
@prop export let ariaLabel = 'double caret left circle';
-->
