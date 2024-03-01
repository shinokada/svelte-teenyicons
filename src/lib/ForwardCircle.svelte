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
  export let ariaLabel = 'forward circle';
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
      d="M8.5 5.5L8.74807 5.06588C8.59332 4.97745 8.40319 4.97808 8.24904 5.06754C8.09488 5.15701 8 5.32176 8 5.5H8.5ZM8.5 9.5H8C8 9.67824 8.09488 9.84299 8.24904 9.93246C8.40319 10.0219 8.59332 10.0226 8.74807 9.93412L8.5 9.5ZM12 7.5L12.2481 7.93412C12.4039 7.8451 12.5 7.67943 12.5 7.5C12.5 7.32057 12.4039 7.1549 12.2481 7.06588L12 7.5ZM4.5 5.5L4.74807 5.06588C4.59332 4.97745 4.40319 4.97808 4.24904 5.06754C4.09488 5.15701 4 5.32176 4 5.5H4.5ZM4.5 9.5H4C4 9.67824 4.09488 9.84299 4.24904 9.93246C4.40319 10.0219 4.59332 10.0226 4.74807 9.93412L4.5 9.5ZM8 7.5L8.24807 7.93412C8.40386 7.8451 8.5 7.67943 8.5 7.5C8.5 7.32057 8.40386 7.1549 8.24807 7.06588L8 7.5ZM7.5 14C3.91015 14 1 11.0899 1 7.5H0C0 11.6421 3.35786 15 7.5 15V14ZM14 7.5C14 11.0899 11.0899 14 7.5 14V15C11.6421 15 15 11.6421 15 7.5H14ZM7.5 1C11.0899 1 14 3.91015 14 7.5H15C15 3.35786 11.6421 0 7.5 0V1ZM7.5 0C3.35786 0 0 3.35786 0 7.5H1C1 3.91015 3.91015 1 7.5 1V0ZM8 5.5V9.5H9V5.5H8ZM8.74807 9.93412L12.2481 7.93412L11.7519 7.06588L8.25193 9.06588L8.74807 9.93412ZM12.2481 7.06588L8.74807 5.06588L8.25193 5.93412L11.7519 7.93412L12.2481 7.06588ZM4 5.5V9.5H5V5.5H4ZM4.74807 9.93412L8.24807 7.93412L7.75193 7.06588L4.25193 9.06588L4.74807 9.93412ZM8.24807 7.06588L4.74807 5.06588L4.25193 5.93412L7.75193 7.93412L8.24807 7.06588Z"
      fill={color}
    />
  {:else}
    <path
      fill-rule="evenodd"
      clip-rule="evenodd"
      d="M0 7.5C0 3.35786 3.35786 0 7.5 0C11.6421 0 15 3.35786 15 7.5C15 11.6421 11.6421 15 7.5 15C3.35786 15 0 11.6421 0 7.5ZM4.24904 5.06754C4.40319 4.97808 4.59332 4.97745 4.74807 5.06588L8 6.92412V5.5C8 5.32176 8.09488 5.15701 8.24904 5.06754C8.40319 4.97808 8.59332 4.97745 8.74807 5.06588L12.2481 7.06588C12.4039 7.1549 12.5 7.32057 12.5 7.5C12.5 7.67943 12.4039 7.8451 12.2481 7.93412L8.74807 9.93412C8.59332 10.0226 8.40319 10.0219 8.24904 9.93246C8.09488 9.84299 8 9.67824 8 9.5V8.07588L4.74807 9.93412C4.59332 10.0226 4.40319 10.0219 4.24904 9.93246C4.09488 9.84299 4 9.67824 4 9.5V5.5C4 5.32176 4.09488 5.15701 4.24904 5.06754Z"
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
@prop export let ariaLabel = 'forward circle';
-->
