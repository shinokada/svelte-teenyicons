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
  export let ariaLabel = 'arrow up circle';
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
      d="M9.14645 6.85355L9.5 7.20711L10.2071 6.5L9.85355 6.14645L9.14645 6.85355ZM7.5 4.5L7.85355 4.14645L7.5 3.79289L7.14645 4.14645L7.5 4.5ZM5.14645 6.14645L4.79289 6.5L5.5 7.20711L5.85355 6.85355L5.14645 6.14645ZM14.5 7.5H14H14.5ZM7.5 14.5V14V14.5ZM7.5 0.5V0V0.5ZM0.5 7.5H0H0.5ZM9.85355 6.14645L7.85355 4.14645L7.14645 4.85355L9.14645 6.85355L9.85355 6.14645ZM7.14645 4.14645L5.14645 6.14645L5.85355 6.85355L7.85355 4.85355L7.14645 4.14645ZM7 4.5V11H8V4.5H7ZM14 7.5C14 11.0899 11.0899 14 7.5 14V15C11.6421 15 15 11.6421 15 7.5H14ZM7.5 1C11.0899 1 14 3.91015 14 7.5H15C15 3.35786 11.6421 -1.78814e-07 7.5 0V1ZM1 7.5C1 3.91015 3.91015 1 7.5 1V0C3.35786 1.78814e-07 -1.78814e-07 3.35786 0 7.5H1ZM0 7.5C1.78814e-07 11.6421 3.35787 15 7.5 15V14C3.91015 14 1 11.0899 1 7.5H0Z"
      fill={color}
    />
  {:else}
    <path
      fill-rule="evenodd"
      clip-rule="evenodd"
      d="M7.49995 15C3.35782 15 -4.55953e-05 11.6421 -4.57764e-05 7.5C-4.59574e-05 3.35786 3.35782 1.81059e-07 7.49995 0C11.6421 -1.81059e-07 15 3.35786 15 7.5C15 11.6421 11.6421 15 7.49995 15ZM4.79292 6.50005L7.50003 3.79294L10.2071 6.50005L9.50003 7.20715L7.99995 5.70708V11H6.99995V5.70723L5.50003 7.20715L4.79292 6.50005Z"
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
@prop export let ariaLabel = 'arrow up circle';
-->
