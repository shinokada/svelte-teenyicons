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
  export let ariaLabel = 'contact';
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
      d="M2 12.5V13H3V12.5H2ZM7 12.5V13H8V12.5H7ZM3 12.5V11.9999H2V12.5H3ZM7 11.9997V12.5H8V11.9997H7ZM5 10C6.10466 10 7 10.8952 7 11.9997H8C8 10.3427 6.65677 9 5 9V10ZM3 11.9999C3 10.8953 3.8954 10 5 10V9C3.34318 9 2 10.343 2 11.9999H3ZM5 4C3.89543 4 3 4.89543 3 6H4C4 5.44772 4.44772 5 5 5V4ZM7 6C7 4.89543 6.10457 4 5 4V5C5.55228 5 6 5.44772 6 6H7ZM5 8C6.10457 8 7 7.10457 7 6H6C6 6.55228 5.55228 7 5 7V8ZM5 7C4.44772 7 4 6.55228 4 6H3C3 7.10457 3.89543 8 5 8V7ZM1.5 3H13.5V2H1.5V3ZM14 3.5V11.5H15V3.5H14ZM13.5 12H1.5V13H13.5V12ZM1 11.5V3.5H0V11.5H1ZM1.5 12C1.22386 12 1 11.7761 1 11.5H0C0 12.3284 0.671574 13 1.5 13V12ZM14 11.5C14 11.7761 13.7761 12 13.5 12V13C14.3284 13 15 12.3284 15 11.5H14ZM13.5 3C13.7761 3 14 3.22386 14 3.5H15C15 2.67157 14.3284 2 13.5 2V3ZM1.5 2C0.671573 2 0 2.67157 0 3.5H1C1 3.22386 1.22386 3 1.5 3V2ZM9 6H12V5H9V6ZM9 9H12V8H9V9ZM0 15H15V14H0V15ZM3 0V2.5H4V0H3ZM11 0V2.5H12V0H11Z"
      fill={color}
    />
  {:else}
    <path
      fill-rule="evenodd"
      clip-rule="evenodd"
      d="M11 2H4V0H3V2H1.5C0.671573 2 0 2.67157 0 3.5V11.5C0 12.3284 0.671574 13 1.5 13H13.5C14.3284 13 15 12.3284 15 11.5V3.5C15 2.67157 14.3284 2 13.5 2H12V0H11V2ZM3 6C3 4.89543 3.89543 4 5 4C6.10457 4 7 4.89543 7 6C7 7.10457 6.10457 8 5 8C3.89543 8 3 7.10457 3 6ZM2.38197 10.618C2.87779 9.6264 3.89132 9 5 9C6.10869 9 7.12222 9.6264 7.61803 10.618L7.94721 11.2764C8.02471 11.4314 8.01643 11.6155 7.92533 11.7629C7.83422 11.9103 7.67329 12 7.5 12H2.5C2.32671 12 2.16578 11.9103 2.07468 11.7629C1.98357 11.6155 1.97529 11.4314 2.05279 11.2764L2.38197 10.618ZM9 6H12V5H9V6ZM9 9H12V8H9V9Z"
      fill={color}
    /> <path d="M15 14V15H0V14H15Z" fill={color} />
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
@prop export let ariaLabel = 'contact';
-->
