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
  export let ariaLabel = 'caret vertical circle';
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
      d="M10.3123 9.39043L10.7028 9.07809L10.0781 8.29722L9.68765 8.60957L10.3123 9.39043ZM7.5 11L7.18765 11.3904L7.5 11.6403L7.81235 11.3904L7.5 11ZM5.31235 8.60957L4.92191 8.29722L4.29722 9.07809L4.68765 9.39043L5.31235 8.60957ZM4.68765 5.60957L4.29722 5.92191L4.92191 6.70278L5.31235 6.39043L4.68765 5.60957ZM7.5 4L7.81235 3.60957L7.5 3.35969L7.18765 3.60957L7.5 4ZM9.68765 6.39043L10.0781 6.70278L10.7028 5.92191L10.3123 5.60957L9.68765 6.39043ZM9.68765 8.60957L7.18765 10.6096L7.81235 11.3904L10.3123 9.39043L9.68765 8.60957ZM7.81235 10.6096L5.31235 8.60957L4.68765 9.39043L7.18765 11.3904L7.81235 10.6096ZM5.31235 6.39043L7.81235 4.39043L7.18765 3.60957L4.68765 5.60957L5.31235 6.39043ZM7.18765 4.39043L9.68765 6.39043L10.3123 5.60957L7.81235 3.60957L7.18765 4.39043ZM7.5 14C3.91015 14 1 11.0899 1 7.5H0C0 11.6421 3.35786 15 7.5 15V14ZM14 7.5C14 11.0899 11.0899 14 7.5 14V15C11.6421 15 15 11.6421 15 7.5H14ZM7.5 1C11.0899 1 14 3.91015 14 7.5H15C15 3.35786 11.6421 0 7.5 0V1ZM7.5 0C3.35786 0 0 3.35786 0 7.5H1C1 3.91015 3.91015 1 7.5 1V0Z"
      fill={color}
    />
  {:else}
    <path
      fill-rule="evenodd"
      clip-rule="evenodd"
      d="M0 7.5C0 3.35786 3.35786 0 7.5 0C11.6421 0 15 3.35786 15 7.5C15 11.6421 11.6421 15 7.5 15C3.35786 15 0 11.6421 0 7.5ZM11 6L7.5 3.375L4 6H11ZM4 9L7.5 11.625L11 9H4Z"
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
@prop export let ariaLabel = 'caret vertical circle';
-->
