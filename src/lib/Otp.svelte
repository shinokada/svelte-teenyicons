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
  export let ariaLabel = 'otp';
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
      d="M6 5.5H9M7.5 5.5V10M10.5 10V7.5M10.5 7.5V5.5H11.5C12.0523 5.5 12.5 5.94772 12.5 6.5C12.5 7.05228 12.0523 7.5 11.5 7.5H10.5ZM4.5 6.5V8.5C4.5 9.05228 4.05228 9.5 3.5 9.5C2.94772 9.5 2.5 9.05228 2.5 8.5V6.5C2.5 5.94772 2.94772 5.5 3.5 5.5C4.05228 5.5 4.5 5.94772 4.5 6.5ZM1.5 0.5H13.5C14.0523 0.5 14.5 0.947715 14.5 1.5V13.5C14.5 14.0523 14.0523 14.5 13.5 14.5H1.5C0.947716 14.5 0.5 14.0523 0.5 13.5V1.5C0.5 0.947716 0.947715 0.5 1.5 0.5Z"
      stroke={color}
    />
  {:else}
    <path
      d="M3.5 6C3.22386 6 3 6.22386 3 6.5V8.5C3 8.77614 3.22386 9 3.5 9C3.77614 9 4 8.77614 4 8.5V6.5C4 6.22386 3.77614 6 3.5 6Z"
      fill={color}
    />
    <path
      d="M11 7H11.5C11.7761 7 12 6.77614 12 6.5C12 6.22386 11.7761 6 11.5 6H11V7Z"
      fill={color}
    />
    <path
      fill-rule="evenodd"
      clip-rule="evenodd"
      d="M0 1.5C0 0.671573 0.671573 0 1.5 0H13.5C14.3284 0 15 0.671573 15 1.5V13.5C15 14.3284 14.3284 15 13.5 15H1.5C0.671573 15 0 14.3284 0 13.5V1.5ZM2 6.5C2 5.67157 2.67157 5 3.5 5C4.32843 5 5 5.67157 5 6.5V8.5C5 9.32843 4.32843 10 3.5 10C2.67157 10 2 9.32843 2 8.5V6.5ZM7 6H6V5H9V6H8V10H7V6ZM10 5H11.5C12.3284 5 13 5.67157 13 6.5C13 7.32843 12.3284 8 11.5 8H11V10H10V5Z"
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
@prop export let ariaLabel = 'otp';
-->
