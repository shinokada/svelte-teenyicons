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
  export let ariaLabel = 'drag horizontal';
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
      d="M3 5.5C3 5.77614 2.77614 6 2.5 6C2.22386 6 2 5.77614 2 5.5C2 5.22386 2.22386 5 2.5 5C2.77614 5 3 5.22386 3 5.5Z"
      stroke={color}
    />
    <path
      d="M8 5.5C8 5.77614 7.77614 6 7.5 6C7.22386 6 7 5.77614 7 5.5C7 5.22386 7.22386 5 7.5 5C7.77614 5 8 5.22386 8 5.5Z"
      stroke={color}
    />
    <path
      d="M13 5.5C13 5.77614 12.7761 6 12.5 6C12.2239 6 12 5.77614 12 5.5C12 5.22386 12.2239 5 12.5 5C12.7761 5 13 5.22386 13 5.5Z"
      stroke={color}
    />
    <path
      d="M3 9.5C3 9.77614 2.77614 10 2.5 10C2.22386 10 2 9.77614 2 9.5C2 9.22386 2.22386 9 2.5 9C2.77614 9 3 9.22386 3 9.5Z"
      stroke={color}
    />
    <path
      d="M8 9.5C8 9.77614 7.77614 10 7.5 10C7.22386 10 7 9.77614 7 9.5C7 9.22386 7.22386 9 7.5 9C7.77614 9 8 9.22386 8 9.5Z"
      stroke={color}
    />
    <path
      d="M13 9.5C13 9.77614 12.7761 10 12.5 10C12.2239 10 12 9.77614 12 9.5C12 9.22386 12.2239 9 12.5 9C12.7761 9 13 9.22386 13 9.5Z"
      stroke={color}
    />
  {:else}
    <path
      fill-rule="evenodd"
      clip-rule="evenodd"
      d="M1.5 5.5C1.5 4.94772 1.94772 4.5 2.5 4.5C3.05228 4.5 3.5 4.94772 3.5 5.5C3.5 6.05228 3.05228 6.5 2.5 6.5C1.94772 6.5 1.5 6.05228 1.5 5.5ZM6.5 5.5C6.5 4.94772 6.94772 4.5 7.5 4.5C8.05228 4.5 8.5 4.94772 8.5 5.5C8.5 6.05228 8.05228 6.5 7.5 6.5C6.94772 6.5 6.5 6.05228 6.5 5.5ZM11.5 5.5C11.5 4.94772 11.9477 4.5 12.5 4.5C13.0523 4.5 13.5 4.94772 13.5 5.5C13.5 6.05228 13.0523 6.5 12.5 6.5C11.9477 6.5 11.5 6.05228 11.5 5.5ZM1.5 9.5C1.5 8.94772 1.94772 8.5 2.5 8.5C3.05228 8.5 3.5 8.94772 3.5 9.5C3.5 10.0523 3.05228 10.5 2.5 10.5C1.94772 10.5 1.5 10.0523 1.5 9.5ZM6.5 9.5C6.5 8.94772 6.94772 8.5 7.5 8.5C8.05228 8.5 8.5 8.94772 8.5 9.5C8.5 10.0523 8.05228 10.5 7.5 10.5C6.94772 10.5 6.5 10.0523 6.5 9.5ZM11.5 9.5C11.5 8.94772 11.9477 8.5 12.5 8.5C13.0523 8.5 13.5 8.94772 13.5 9.5C13.5 10.0523 13.0523 10.5 12.5 10.5C11.9477 10.5 11.5 10.0523 11.5 9.5Z"
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
@prop export let ariaLabel = 'drag horizontal';
-->
