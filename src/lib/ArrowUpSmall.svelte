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
  export let ariaLabel = 'arrow up small';
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
      d="M5.14645 6.14645L4.79289 6.5L5.5 7.20711L5.85355 6.85355L5.14645 6.14645ZM7.5 4.5L7.85355 4.14645L7.5 3.79289L7.14645 4.14645L7.5 4.5ZM9.14645 6.85355L9.5 7.20711L10.2071 6.5L9.85355 6.14645L9.14645 6.85355ZM5.85355 6.85355L7.85355 4.85355L7.14645 4.14645L5.14645 6.14645L5.85355 6.85355ZM7.14645 4.85355L9.14645 6.85355L9.85355 6.14645L7.85355 4.14645L7.14645 4.85355ZM7 4.5V11H8V4.5H7Z"
      fill={color}
    />
  {:else}
    <path
      fill-rule="evenodd"
      clip-rule="evenodd"
      d="M7.50001 3.79291L10.2071 6.50001L9.50001 7.20712L8.00001 5.70712V11H7.00001V5.70712L5.50001 7.20712L4.7929 6.50001L7.50001 3.79291Z"
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
@prop export let ariaLabel = 'arrow up small';
-->
