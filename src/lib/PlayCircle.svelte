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
  export let ariaLabel = 'play circle';
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
      d="M6.5 5.5L6.74807 5.06588C6.59332 4.97745 6.40319 4.97808 6.24904 5.06754C6.09488 5.15701 6 5.32176 6 5.5H6.5ZM6.5 9.5H6C6 9.67824 6.09488 9.84299 6.24904 9.93246C6.40319 10.0219 6.59332 10.0226 6.74807 9.93412L6.5 9.5ZM10 7.5L10.2481 7.93412C10.4039 7.8451 10.5 7.67943 10.5 7.5C10.5 7.32057 10.4039 7.1549 10.2481 7.06588L10 7.5ZM7.5 14C3.91015 14 1 11.0899 1 7.5H0C0 11.6421 3.35786 15 7.5 15V14ZM14 7.5C14 11.0899 11.0899 14 7.5 14V15C11.6421 15 15 11.6421 15 7.5H14ZM7.5 1C11.0899 1 14 3.91015 14 7.5H15C15 3.35786 11.6421 0 7.5 0V1ZM7.5 0C3.35786 0 0 3.35786 0 7.5H1C1 3.91015 3.91015 1 7.5 1V0ZM6 5.5V9.5H7V5.5H6ZM6.74807 9.93412L10.2481 7.93412L9.75193 7.06588L6.25193 9.06588L6.74807 9.93412ZM10.2481 7.06588L6.74807 5.06588L6.25193 5.93412L9.75193 7.93412L10.2481 7.06588Z"
      fill={color}
    />
  {:else}
    <path
      fill-rule="evenodd"
      clip-rule="evenodd"
      d="M0 7.5C0 3.35786 3.35786 0 7.5 0C11.6421 0 15 3.35786 15 7.5C15 11.6421 11.6421 15 7.5 15C3.35786 15 0 11.6421 0 7.5ZM6.24904 5.06754C6.40319 4.97808 6.59332 4.97745 6.74807 5.06588L10.2481 7.06588C10.4039 7.1549 10.5 7.32057 10.5 7.5C10.5 7.67943 10.4039 7.8451 10.2481 7.93412L6.74807 9.93412C6.59332 10.0226 6.40319 10.0219 6.24904 9.93246C6.09488 9.84299 6 9.67824 6 9.5V5.5C6 5.32176 6.09488 5.15701 6.24904 5.06754Z"
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
@prop export let ariaLabel = 'play circle';
-->
