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
  export let ariaLabel = 'gatsbyjs';
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
      d="M11.0707 4C10.1632 3.07432 8.89868 2.5 7.49998 2.5C5.26116 2.5 3.36601 3.97145 2.72888 6L8.99998 12.2711C10.8756 11.682 12.275 10.0174 12.4753 8H8.99998M2.5 8.5L6.5 12.5M7.5 14.5C3.63401 14.5 0.5 11.366 0.5 7.5C0.5 3.63401 3.63401 0.5 7.5 0.5C11.366 0.5 14.5 3.63401 14.5 7.5C14.5 11.366 11.366 14.5 7.5 14.5Z"
      stroke={color}
    />
  {:else}
    <path
      fill-rule="evenodd"
      clip-rule="evenodd"
      d="M0 7.5C0 3.35786 3.35786 0 7.5 0C11.6421 0 15 3.35786 15 7.5C15 11.6421 11.6421 15 7.5 15C3.35786 15 0 11.6421 0 7.5ZM3.30472 5.86865C3.95815 4.18936 5.5908 3 7.50006 3C8.75899 3 9.89643 3.51632 10.7137 4.35002L11.4278 3.64998C10.4302 2.63232 9.03852 2 7.50006 2C5.0366 2 2.95264 3.61922 2.25194 5.85017L2.16113 6.13928L8.86078 12.8389L9.14988 12.7481C11.2129 12.1002 12.7525 10.2699 12.9729 8.0494L13.0275 7.5H9.00006V8.5H11.8886C11.5562 9.96491 10.5084 11.1595 9.1314 11.6953L3.30472 5.86865ZM6.14648 12.8536L2.14648 8.85359L2.85359 8.14648L6.85359 12.1465L6.14648 12.8536Z"
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
@prop export let ariaLabel = 'gatsbyjs';
-->
