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
  export let ariaLabel = 'sim';
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
      d="M4 5.5H7.5V12M4 8.5H6M4 11.5H6M9 5.5H11M9 8.5H11M9 11.5H11M12.5 14.5H2.5C1.94771 14.5 1.5 14.0523 1.5 13.5V1.5C1.5 0.947716 1.94771 0.5 2.5 0.5H9.5L13.5 4.5V13.5C13.5 14.0523 13.0523 14.5 12.5 14.5Z"
      stroke={color}
    />
  {:else}
    <path
      fill-rule="evenodd"
      clip-rule="evenodd"
      d="M9.70711 0H2.5C1.67157 0 1 0.671574 1 1.5V13.5C1 14.3284 1.67157 15 2.5 15H12.5C13.3284 15 14 14.3284 14 13.5V4.29289L9.70711 0ZM7 6H4V5H8V12H7V6ZM6 9H4V8H6V9ZM4 12H6V11H4V12ZM11 6H9V5H11V6ZM9 9H11V8H9V9ZM11 12H9V11H11V12Z"
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
@prop export let ariaLabel = 'sim';
-->
