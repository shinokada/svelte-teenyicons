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
  export let ariaLabel = 'ms excel';
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
      d="M2.5 3.5V1.5C2.5 0.947715 2.94772 0.5 3.5 0.5H13.5C14.0523 0.5 14.5 0.947715 14.5 1.5V13.5C14.5 14.0523 14.0523 14.5 13.5 14.5H3.5C2.94772 14.5 2.5 14.0523 2.5 13.5V11.5M2.5 5.5L6.5 9.5M2.5 9.5L6.5 5.5M1.5 3.5H7.5C8.05228 3.5 8.5 3.94772 8.5 4.5V10.5C8.5 11.0523 8.05228 11.5 7.5 11.5H1.5C0.947715 11.5 0.5 11.0523 0.5 10.5V4.5C0.5 3.94772 0.947715 3.5 1.5 3.5Z"
      stroke={color}
    />
  {:else}
    <path
      d="M3.79293 7.49998L2.14648 5.85353L2.85359 5.14642L4.50004 6.79287L6.14648 5.14642L6.85359 5.85353L5.20714 7.49998L6.85359 9.14642L6.14648 9.85353L4.50004 8.20708L2.85359 9.85353L2.14648 9.14642L3.79293 7.49998Z"
      fill={color}
    />
    <path
      fill-rule="evenodd"
      clip-rule="evenodd"
      d="M3.5 0C2.67157 0 2 0.671573 2 1.5V3H1.5C0.671573 3 0 3.67157 0 4.5V10.5C0 11.3284 0.671573 12 1.5 12H2V13.5C2 14.3284 2.67157 15 3.5 15H13.5C14.3284 15 15 14.3284 15 13.5V1.5C15 0.671573 14.3284 0 13.5 0H3.5ZM1.5 4C1.22386 4 1 4.22386 1 4.5V10.5C1 10.7761 1.22386 11 1.5 11H7.5C7.77614 11 8 10.7761 8 10.5V4.5C8 4.22386 7.77614 4 7.5 4H1.5Z"
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
@prop export let ariaLabel = 'ms excel';
-->
