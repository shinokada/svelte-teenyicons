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
  export let ariaLabel = 'behance';
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
      d="M14.5 9.5V10H15V9.5H14.5ZM0.5 2.5V2H0V2.5H0.5ZM0.5 12.5H0V13H0.5V12.5ZM8 9.5C8 11.433 9.567 13 11.5 13V12C10.1193 12 9 10.8807 9 9.5H8ZM11.5 6C9.567 6 8 7.567 8 9.5H9C9 8.11929 10.1193 7 11.5 7V6ZM15 9.5C15 7.567 13.433 6 11.5 6V7C12.8807 7 14 8.11929 14 9.5H15ZM13.5268 10.964C13.0717 11.5927 12.3334 12 11.5 12V13C12.6677 13 13.7018 12.4276 14.3368 11.5504L13.5268 10.964ZM0.5 3H3V2H0.5V3ZM3 7H0.5V8H3V7ZM1 7.5V2.5H0V7.5H1ZM5 5C5 6.10457 4.10457 7 3 7V8C4.65685 8 6 6.65685 6 5H5ZM3 3C4.10457 3 5 3.89543 5 5H6C6 3.34315 4.65685 2 3 2V3ZM0.5 8H4V7H0.5V8ZM4 12H0.5V13H4V12ZM1 12.5V7.5H0V12.5H1ZM6 10C6 11.1046 5.10457 12 4 12V13C5.65685 13 7 11.6569 7 10H6ZM4 8C5.10457 8 6 8.89543 6 10H7C7 8.34315 5.65685 7 4 7V8ZM8.5 10H14.5V9H8.5V10ZM9 4H14V3H9V4Z"
      fill={color}
    />
  {:else}
    <path
      fill-rule="evenodd"
      clip-rule="evenodd"
      d="M0 2H3C4.65685 2 6 3.34315 6 5C6 5.86358 5.63511 6.64193 5.05111 7.1893C6.18952 7.61522 7 8.71296 7 10C7 11.6569 5.65685 13 4 13H0V2ZM1 8V12H4C5.10457 12 6 11.1046 6 10C6 8.89543 5.10457 8 4 8H1ZM1 7H3C4.10457 7 5 6.10457 5 5C5 3.89543 4.10457 3 3 3H1V7ZM14 4H9V3H14V4ZM8 9.5C8 7.567 9.567 6 11.5 6C13.433 6 15 7.567 15 9.5V10H9.05001C9.28164 11.1411 10.2905 12 11.5 12C12.3334 12 13.0717 11.5927 13.5268 10.964L14.3368 11.5504C13.7018 12.4276 12.6677 13 11.5 13C9.567 13 8 11.433 8 9.5ZM9.05001 9H13.95C13.7184 7.85888 12.7095 7 11.5 7C10.2905 7 9.28164 7.85888 9.05001 9Z"
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
@prop export let ariaLabel = 'behance';
-->
