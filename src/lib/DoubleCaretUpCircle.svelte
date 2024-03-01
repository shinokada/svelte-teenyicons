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
  export let ariaLabel = 'double caret up circle';
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
      d="M5.14645 6.14645L4.79289 6.5L5.5 7.20711L5.85355 6.85355L5.14645 6.14645ZM7.5 4.5L7.85355 4.14645L7.5 3.79289L7.14645 4.14645L7.5 4.5ZM9.14645 6.85355L9.5 7.20711L10.2071 6.5L9.85355 6.14645L9.14645 6.85355ZM5.14645 9.14645L4.79289 9.5L5.5 10.2071L5.85355 9.85355L5.14645 9.14645ZM7.5 7.5L7.85355 7.14645L7.5 6.79289L7.14645 7.14645L7.5 7.5ZM9.14645 9.85355L9.5 10.2071L10.2071 9.5L9.85355 9.14645L9.14645 9.85355ZM0.5 7.5H0H0.5ZM7.5 14.5V15V14.5ZM7.5 0.5V1V0.5ZM14.5 7.5H14H14.5ZM5.85355 6.85355L7.85355 4.85355L7.14645 4.14645L5.14645 6.14645L5.85355 6.85355ZM7.14645 4.85355L9.14645 6.85355L9.85355 6.14645L7.85355 4.14645L7.14645 4.85355ZM5.85355 9.85355L7.85355 7.85355L7.14645 7.14645L5.14645 9.14645L5.85355 9.85355ZM7.14645 7.85355L9.14645 9.85355L9.85355 9.14645L7.85355 7.14645L7.14645 7.85355ZM0 7.5C-5.96046e-08 11.6421 3.35786 15 7.5 15V14C3.91015 14 1 11.0899 1 7.5H0ZM7.5 0C3.35786 -5.96046e-08 5.96046e-08 3.35786 0 7.5H1C1 3.91015 3.91015 1 7.5 1V0ZM15 7.5C15 3.35786 11.6421 5.96046e-08 7.5 0V1C11.0899 1 14 3.91015 14 7.5H15ZM14 7.5C14 11.0899 11.0899 14 7.5 14V15C11.6421 15 15 11.6421 15 7.5H14Z"
      fill={color}
    />
  {:else}
    <path
      fill-rule="evenodd"
      clip-rule="evenodd"
      d="M7.5 14.9999C11.6421 14.9999 15 11.6421 15 7.49994C15 3.3578 11.6421 -6.09858e-05 7.5 -6.10352e-05C3.35786 -6.10846e-05 4.93949e-08 3.3578 0 7.49994C-4.9394e-08 11.6421 3.35786 14.9999 7.5 14.9999ZM10.207 9.49999L7.49992 6.79288L4.79282 9.49999L5.49992 10.2071L7.49992 8.20709L9.49992 10.2071L10.207 9.49999ZM10.207 6.49999L7.49992 3.79288L4.79282 6.49999L5.49992 7.20709L7.49992 5.20709L9.49992 7.20709L10.207 6.49999Z"
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
@prop export let ariaLabel = 'double caret up circle';
-->
