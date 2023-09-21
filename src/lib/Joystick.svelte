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
  export let ariaLabel = 'joystick';
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
      d="M1.5 10.5V10C1.22386 10 1 10.2239 1 10.5H1.5ZM13.5 10.5H14C14 10.2239 13.7761 10 13.5 10V10.5ZM13.5 14.5V15C13.7761 15 14 14.7761 14 14.5H13.5ZM1.5 14.5H1C1 14.7761 1.22386 15 1.5 15V14.5ZM1.5 11H13.5V10H1.5V11ZM13 10.5V14.5H14V10.5H13ZM13.5 14H1.5V15H13.5V14ZM2 14.5V10.5H1V14.5H2ZM8 10.5V6.5H7V10.5H8ZM7.5 0C5.567 0 4 1.567 4 3.5H5C5 2.11929 6.11929 1 7.5 1V0ZM11 3.5C11 1.567 9.433 0 7.5 0V1C8.88071 1 10 2.11929 10 3.5H11ZM7.5 7C9.433 7 11 5.433 11 3.5H10C10 4.88071 8.88071 6 7.5 6V7ZM7.5 6C6.11929 6 5 4.88071 5 3.5H4C4 5.433 5.567 7 7.5 7V6ZM3 9H5V8H3V9Z"
      fill={color}
    />
  {:else}
    <path
      d="M4 3.5C4 1.567 5.567 0 7.5 0C9.433 0 11 1.567 11 3.5C11 5.26324 9.69615 6.72194 8 6.96456V10H13.5C13.7761 10 14 10.2239 14 10.5V14.5C14 14.7761 13.7761 15 13.5 15H1.5C1.22386 15 1 14.7761 1 14.5V10.5C1 10.2239 1.22386 10 1.5 10H7V6.96456C5.30385 6.72194 4 5.26324 4 3.5Z"
      fill={color}
    /> <path d="M3 8V9H5V8H3Z" fill={color} />
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
@prop export let ariaLabel = 'joystick';
-->
