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
  export let ariaLabel = 'cup';
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
      d="M11.5 6.5V11.5C11.5 13.1569 10.1569 14.5 8.5 14.5H3.5C1.84315 14.5 0.5 13.1569 0.5 11.5V6.5C0.5 5.94772 0.947715 5.5 1.5 5.5H10.5C11.0523 5.5 11.5 5.94772 11.5 6.5ZM11.5 6.5H13.5C14.0523 6.5 14.5 6.94772 14.5 7.5V9.5C14.5 10.0523 14.0523 10.5 13.5 10.5H11.5M4.5 4V2M7.5 4V0"
      stroke={color}
    />
  {:else}
    <path d="M7 4H8V0H7V4Z" fill={color} /> <path d="M5 2V4H4V2H5Z" fill={color} />
    <path
      fill-rule="evenodd"
      clip-rule="evenodd"
      d="M0 6.5C0 5.67157 0.671573 5 1.5 5H10.5C11.1531 5 11.7087 5.4174 11.9146 6H13.5C14.3284 6 15 6.67157 15 7.5V9.5C15 10.3284 14.3284 11 13.5 11H12V11.5C12 13.433 10.433 15 8.5 15H3.5C1.567 15 0 13.433 0 11.5V6.5ZM12 10H13.5C13.7761 10 14 9.77614 14 9.5V7.5C14 7.22386 13.7761 7 13.5 7H12V10Z"
      fill={color}
    />
  {/if}
</svg>

<!--
@component
[Go to docs](https://svelte-teenyicons.vercel.app/)
## Props
@prop export let size: string = ctx.size || '15';
@prop export let role: string = ctx.role || 'img';
@prop export let color: string = ctx.color || 'currentColor';
@prop export let variation: 'solid' | 'outline' = 'outline';
@prop export let ariaLabel = 'cup';
-->
