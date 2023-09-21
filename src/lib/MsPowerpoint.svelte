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
  export let ariaLabel = 'ms powerpoint';
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
      d="M1.75464 3.5C3.01958 1.68652 5.1212 0.5 7.49995 0.5C11.3659 0.5 14.4999 3.63401 14.4999 7.5C14.4999 11.366 11.3659 14.5 7.49995 14.5C5.1212 14.5 3.01958 13.3135 1.75464 11.5M2.5 10V8.5M2.5 8.5V5.5H5C5.82843 5.5 6.5 6.17157 6.5 7C6.5 7.82843 5.82843 8.5 5 8.5H2.5ZM1.5 3.5H7.5C8.05228 3.5 8.5 3.94772 8.5 4.5V10.5C8.5 11.0523 8.05228 11.5 7.5 11.5H1.5C0.947715 11.5 0.5 11.0523 0.5 10.5V4.5C0.5 3.94772 0.947715 3.5 1.5 3.5Z"
      stroke={color}
    />
  {:else}
    <path
      fill-rule="evenodd"
      clip-rule="evenodd"
      d="M5 5H2V10H3V9H5C6.10457 9 7 8.10457 7 7C7 5.89543 6.10457 5 5 5ZM5 8H3V6H5C5.55228 6 6 6.44772 6 7C6 7.55228 5.55228 8 5 8Z"
      fill={color}
    />
    <path
      fill-rule="evenodd"
      clip-rule="evenodd"
      d="M7.49983 0C5.0456 0 2.86687 1.17924 1.49932 3C0.671208 3.00037 0 3.6718 0 4.5V10.5C0 11.3282 0.671206 11.9996 1.49932 12C2.86687 13.8208 5.0456 15 7.49983 15C11.642 15 14.9998 11.6421 14.9998 7.5C14.9998 3.35786 11.642 0 7.49983 0ZM1 4.5C1 4.22386 1.22386 4 1.5 4H7.5C7.77165 4 7.99269 4.21663 7.99982 4.48655V10.5134C7.99269 10.7834 7.77165 11 7.5 11H1.5C1.22386 11 1 10.7761 1 10.5V4.5Z"
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
@prop export let ariaLabel = 'ms powerpoint';
-->
