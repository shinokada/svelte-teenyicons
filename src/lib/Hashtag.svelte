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
  export let ariaLabel = 'hashtag';
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
    <path d="M2 5.5H13M2 9.5H13M6.5 1.5L4.5 13.5M10.5 1.5L8.5 13.5" stroke={color} />
  {:else}
    <path
      fill-rule="evenodd"
      clip-rule="evenodd"
      d="M5.40977 5L6.0068 1.4178L6.9932 1.5822L6.42356 5H9.40977L10.0068 1.4178L10.9932 1.5822L10.4236 5H13V6H10.2569L9.7569 9H13V10H9.59023L8.9932 13.5822L8.0068 13.4178L8.57644 10H5.59023L4.9932 13.5822L4.0068 13.4178L4.57644 10H2V9H4.7431L5.2431 6H2V5H5.40977ZM6.2569 6L5.7569 9H8.7431L9.2431 6H6.2569Z"
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
@prop export let ariaLabel = 'hashtag';
-->
