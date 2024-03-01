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
  export let ariaLabel = 'lan cable';
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
      d="M6.5 11.5V15M8.5 11.5V15M6 9.5H9M6.5 0.5V2.5H8.5V0.5M4.5 0.5H10.5V4.5H11.5V7.5L9.5 11.5H5.5L3.5 7.5V4.5H4.5V0.5ZM6.5 4.5V6.5C6.5 7.05228 6.94772 7.5 7.5 7.5C8.05228 7.5 8.5 7.05228 8.5 6.5V4.5H6.5Z"
      stroke={color}
    />
  {:else}
    <path d="M7 6.5V5H8V6.5C8 6.77614 7.77614 7 7.5 7C7.22386 7 7 6.77614 7 6.5Z" fill={color} />
    <path
      fill-rule="evenodd"
      clip-rule="evenodd"
      d="M9 0H11V4H12V7.61803L9.80902 12H9V15H8V12H7V15H6V12H5.19098L3 7.61803V4H4V0H6V3H9V0ZM9 4H6V6.5C6 7.32843 6.67157 8 7.5 8C8.32843 8 9 7.32843 9 6.5V4ZM6 9V10H9V9H6Z"
      fill={color}
    /> <path d="M8 0H7V2H8V0Z" fill={color} />
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
@prop export let ariaLabel = 'lan cable';
-->
