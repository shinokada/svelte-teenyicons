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
  export let ariaLabel = 'gbc';
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
      d="M4.5 2.5V2C4.22386 2 4 2.22386 4 2.5H4.5ZM10.5 2.5H11C11 2.22386 10.7761 2 10.5 2V2.5ZM4.5 6.5H4C4 6.77614 4.22386 7 4.5 7V6.5ZM3.5 1H11.5V0H3.5V1ZM12 1.5V11.5H13V1.5H12ZM9.5 14H3.5V15H9.5V14ZM3 13.5V1.5H2V13.5H3ZM3.5 14C3.22386 14 3 13.7761 3 13.5H2C2 14.3284 2.67157 15 3.5 15V14ZM12 11.5C12 12.8807 10.8807 14 9.5 14V15C11.433 15 13 13.433 13 11.5H12ZM11.5 1C11.7761 1 12 1.22386 12 1.5H13C13 0.671573 12.3284 0 11.5 0V1ZM3.5 0C2.67157 0 2 0.671574 2 1.5H3C3 1.22386 3.22386 1 3.5 1V0ZM4.5 3H10.5V2H4.5V3ZM10 2.5V5.5H11V2.5H10ZM9.5 6H4.5V7H9.5V6ZM5 6.5V2.5H4V6.5H5ZM10 5.5C10 5.77614 9.77614 6 9.5 6V7C10.3284 7 11 6.32843 11 5.5H10ZM5 8V11H6V8H5ZM4 10H7V9H4V10ZM10 9H11V8H10V9ZM9 11H10V10H9V11Z"
      fill={color}
    />
  {:else}
    <path d="M5 6V3H10V5.5C10 5.77614 9.77614 6 9.5 6H5Z" fill={color} />
    <path
      fill-rule="evenodd"
      clip-rule="evenodd"
      d="M2 1.5C2 0.671573 2.67157 0 3.5 0H11.5C12.3284 0 13 0.671573 13 1.5V11.5C13 13.433 11.433 15 9.5 15H3.5C2.67157 15 2 14.3284 2 13.5V1.5ZM4.5 2C4.22386 2 4 2.22386 4 2.5V6.5C4 6.77614 4.22386 7 4.5 7H9.5C10.3284 7 11 6.32843 11 5.5V2.5C11 2.22386 10.7761 2 10.5 2H4.5ZM5 8V9H4V10H5V11H6V10H7V9H6V8H5ZM10 8V9H11V8H10ZM9 11V10H10V11H9Z"
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
@prop export let ariaLabel = 'gbc';
-->
