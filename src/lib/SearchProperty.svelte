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
  export let ariaLabel = 'search property';
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
      d="M4.5 8.5H4C4 8.77614 4.22386 9 4.5 9V8.5ZM8.5 8.5V9C8.77614 9 9 8.77614 9 8.5H8.5ZM8.5 6H9C9 5.86739 8.94732 5.74021 8.85355 5.64645L8.5 6ZM6.5 4L6.85355 3.64645C6.65829 3.45118 6.34171 3.45118 6.14645 3.64645L6.5 4ZM4.5 6L4.14645 5.64645C4.05268 5.74021 4 5.86739 4 6H4.5ZM14.8536 14.1464L10.8536 10.1464L10.1464 10.8536L14.1464 14.8536L14.8536 14.1464ZM6.5 12C3.46243 12 1 9.53757 1 6.5H0C0 10.0899 2.91015 13 6.5 13V12ZM12 6.5C12 9.53757 9.53757 12 6.5 12V13C10.0899 13 13 10.0899 13 6.5H12ZM6.5 1C9.53757 1 12 3.46243 12 6.5H13C13 2.91015 10.0899 0 6.5 0V1ZM6.5 0C2.91015 0 0 2.91015 0 6.5H1C1 3.46243 3.46243 1 6.5 1V0ZM4.5 9H8.5V8H4.5V9ZM9 8.5V6H8V8.5H9ZM8.85355 5.64645L6.85355 3.64645L6.14645 4.35355L8.14645 6.35355L8.85355 5.64645ZM6.14645 3.64645L4.14645 5.64645L4.85355 6.35355L6.85355 4.35355L6.14645 3.64645ZM4 6V8.5H5V6H4Z"
      fill={color}
    />
  {:else}
    <path d="M5 8V6.20711L6.5 4.70711L8 6.20711V8H5Z" fill={color} />
    <path
      fill-rule="evenodd"
      clip-rule="evenodd"
      d="M0 6.5C0 2.91015 2.91015 0 6.5 0C10.0899 0 13 2.91015 13 6.5C13 8.11493 12.4111 9.59231 11.4362 10.7291L14.8536 14.1464L14.1465 14.8535L10.7291 11.4362C9.59237 12.411 8.11496 13 6.5 13C2.91015 13 0 10.0899 0 6.5ZM8.85355 5.64645L6.85355 3.64645C6.65829 3.45118 6.34171 3.45118 6.14645 3.64645L4.14645 5.64645C4.05268 5.74021 4 5.86739 4 6V8.5C4 8.77614 4.22386 9 4.5 9H8.5C8.77614 9 9 8.77614 9 8.5V6C9 5.86739 8.94732 5.74021 8.85355 5.64645Z"
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
@prop export let ariaLabel = 'search property';
-->
