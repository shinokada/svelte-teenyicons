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
  export let ariaLabel = 'chat';
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
      d="M11.5 13.5L11.6568 13.0252L11.4388 12.9532L11.2421 13.0716L11.5 13.5ZM13.5 11.5L13.0788 11.2305L12.95 11.4319L13.0258 11.6585L13.5 11.5ZM14.5 14.4908L14.3432 14.9656C14.5229 15.025 14.7206 14.9778 14.8542 14.8437C14.9878 14.7097 15.0342 14.5118 14.9742 14.3323L14.5 14.4908ZM11.2421 13.0716C10.2859 13.6474 8.75657 13.9908 7.5 13.9908V14.9908C8.88543 14.9908 10.6061 14.6218 11.7579 13.9284L11.2421 13.0716ZM7.5 13.9908C3.90983 13.9908 1 11.0825 1 7.49548H0C0 11.6354 3.35817 14.9908 7.5 14.9908V13.9908ZM1 7.49548C1 3.90845 3.90984 1 7.5 1V0C3.35816 0 0 3.35556 0 7.49548H1ZM7.5 1C11.0902 1 14 3.90845 14 7.49548H15C15 3.35556 11.6418 0 7.5 0V1ZM14 7.49548C14 8.82628 13.7043 10.2529 13.0788 11.2305L13.9212 11.7695C14.6857 10.5745 15 8.93686 15 7.49548H14ZM11.3432 13.9748L14.3432 14.9656L14.6568 14.0161L11.6568 13.0252L11.3432 13.9748ZM14.9742 14.3323L13.9742 11.3415L13.0258 11.6585L14.0258 14.6494L14.9742 14.3323Z"
      fill={color}
    />
  {:else}
    <path
      d="M7.5 0C3.35816 0 0 3.35556 0 7.49548C0 11.6354 3.35817 14.9908 7.5 14.9908C8.80596 14.9908 10.4098 14.6629 11.5542 14.0445L14.3432 14.9656C14.5229 15.025 14.7206 14.9778 14.8542 14.8437C14.9878 14.7097 15.0342 14.5118 14.9742 14.3323L14.0476 11.5609C14.7205 10.3884 15 8.85469 15 7.49548C15 3.35556 11.6418 0 7.5 0Z"
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
@prop export let ariaLabel = 'chat';
-->
