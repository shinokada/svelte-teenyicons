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
  export let ariaLabel = 'area chart';
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
      d="M0.5 14.5H0V15H0.5V14.5ZM6.5 5.5L6.9 5.2C6.80264 5.07018 6.64833 4.99569 6.48613 5.00019C6.32392 5.00469 6.17399 5.08763 6.08397 5.22265L6.5 5.5ZM9.5 9.5L9.1 9.8C9.19566 9.92754 9.3464 10.0018 9.50581 9.99997C9.66523 9.99811 9.8142 9.92035 9.90687 9.79062L9.5 9.5ZM0 0V14.5H1V0H0ZM0.5 15H15V14H0.5V15ZM2.91603 11.7774L6.91603 5.77735L6.08397 5.22265L2.08397 11.2226L2.91603 11.7774ZM6.1 5.8L9.1 9.8L9.9 9.2L6.9 5.2L6.1 5.8ZM9.90687 9.79062L14.9069 2.79062L14.0931 2.20938L9.09313 9.20938L9.90687 9.79062Z"
      fill={color}
    />
  {:else}
    <path
      d="M1 0H0V14.5C0 14.5 0 14.5 0 14.5V15H0.497812C0.498541 15 0.499271 15 0.500001 15H14.5C14.5007 15 14.5015 15 14.5022 15H15V14.501C15 14.5013 15 14.5007 15 14.501L15 2.5C15 2.28265 14.8596 2.09019 14.6526 2.02386C14.4456 1.95752 14.2195 2.03252 14.0931 2.20939L9.49016 8.65355L6.9 5.2C6.80264 5.07019 6.64833 4.99569 6.48613 5.0002C6.32392 5.0047 6.17399 5.08764 6.08398 5.22265L1 12.8486V0Z"
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
@prop export let ariaLabel = 'area chart';
-->
