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
  export let ariaLabel = 'artboard';
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
      d="M4.5 4.5V4C4.22386 4 4 4.22386 4 4.5H4.5ZM10.5 4.5H11C11 4.22386 10.7761 4 10.5 4V4.5ZM10.5 10.5V11C10.7761 11 11 10.7761 11 10.5H10.5ZM4.5 10.5H4C4 10.7761 4.22386 11 4.5 11V10.5ZM4 0V2H5V0H4ZM10 0V2H11V0H10ZM0 5H2V4H0V5ZM0 11H2V10H0V11ZM13 5H15V4H13V5ZM13 11H15V10H13V11ZM4 13V15H5V13H4ZM10 13V15H11V13H10ZM4.5 5H10.5V4H4.5V5ZM10 4.5V10.5H11V4.5H10ZM10.5 10H4.5V11H10.5V10ZM5 10.5V4.5H4V10.5H5Z"
      fill={color}
    />
  {:else}
    <path d="M4 0V2H5V0H4Z" fill={color} /> <path d="M10 0V2H11V0H10Z" fill={color} />
    <path d="M2 5H0V4H2V5Z" fill={color} /> <path d="M0 11H2V10H0V11Z" fill={color} />
    <path d="M15 5H13V4H15V5Z" fill={color} /> <path d="M13 11H15V10H13V11Z" fill={color} />
    <path d="M4 15V13H5V15H4Z" fill={color} /> <path d="M10 13V15H11V13H10Z" fill={color} />
    <path
      d="M4.5 4C4.22386 4 4 4.22386 4 4.5V10.5C4 10.7761 4.22386 11 4.5 11H10.5C10.7761 11 11 10.7761 11 10.5V4.5C11 4.22386 10.7761 4 10.5 4H4.5Z"
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
@prop export let ariaLabel = 'artboard';
-->
