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
  export let ariaLabel = 'qr code';
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
      d="M12 8.5H8.5V12M14 8.5H15M12 14.5H8M11 11.5H14.5V15M3 3.5H4M11 3.5H12M3 11.5H4M1.5 0.5H5.5C6.05228 0.5 6.5 0.947715 6.5 1.5V5.5C6.5 6.05228 6.05228 6.5 5.5 6.5H1.5C0.947715 6.5 0.5 6.05228 0.5 5.5V1.5C0.5 0.947715 0.947715 0.5 1.5 0.5ZM9.5 0.5H13.5C14.0523 0.5 14.5 0.947715 14.5 1.5V5.5C14.5 6.05228 14.0523 6.5 13.5 6.5H9.5C8.94772 6.5 8.5 6.05228 8.5 5.5V1.5C8.5 0.947715 8.94772 0.5 9.5 0.5ZM1.5 8.5H5.5C6.05228 8.5 6.5 8.94772 6.5 9.5V13.5C6.5 14.0523 6.05228 14.5 5.5 14.5H1.5C0.947715 14.5 0.5 14.0523 0.5 13.5V9.5C0.5 8.94772 0.947715 8.5 1.5 8.5Z"
      stroke={color}
    />
  {:else}
    <path
      fill-rule="evenodd"
      clip-rule="evenodd"
      d="M0 1.5C0 0.671573 0.671573 0 1.5 0H5.5C6.32843 0 7 0.671573 7 1.5V5.5C7 6.32843 6.32843 7 5.5 7H1.5C0.671573 7 0 6.32843 0 5.5V1.5ZM1.5 1C1.22386 1 1 1.22386 1 1.5V5.5C1 5.77614 1.22386 6 1.5 6H5.5C5.77614 6 6 5.77614 6 5.5V1.5C6 1.22386 5.77614 1 5.5 1H1.5ZM8 1.5C8 0.671573 8.67157 0 9.5 0H13.5C14.3284 0 15 0.671573 15 1.5V5.5C15 6.32843 14.3284 7 13.5 7H9.5C8.67157 7 8 6.32843 8 5.5V1.5ZM9.5 1C9.22386 1 9 1.22386 9 1.5V5.5C9 5.77614 9.22386 6 9.5 6H13.5C13.7761 6 14 5.77614 14 5.5V1.5C14 1.22386 13.7761 1 13.5 1H9.5ZM4 4H3V3H4V4ZM12 4H11V3H12V4ZM0 9.5C0 8.67157 0.671573 8 1.5 8H5.5C6.32843 8 7 8.67157 7 9.5V13.5C7 14.3284 6.32843 15 5.5 15H1.5C0.671573 15 0 14.3284 0 13.5V9.5ZM1.5 9C1.22386 9 1 9.22386 1 9.5V13.5C1 13.7761 1.22386 14 1.5 14H5.5C5.77614 14 6 13.7761 6 13.5V9.5C6 9.22386 5.77614 9 5.5 9H1.5ZM8 8H12V9H9V12H8V8ZM15 9H14V8H15V9ZM4 12H3V11H4V12ZM14 12H11V11H15V15H14V12ZM8 14H12V15H8V14Z"
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
@prop export let ariaLabel = 'qr code';
-->
