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
  export let ariaLabel = 'edit small';
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
      d="M4.5 8.5L4.14645 8.14645L4 8.29289V8.5H4.5ZM8.5 4.5L8.85355 4.14645C8.65829 3.95118 8.34171 3.95118 8.14645 4.14645L8.5 4.5ZM10.5 6.5L10.8536 6.85355C11.0488 6.65829 11.0488 6.34171 10.8536 6.14645L10.5 6.5ZM6.5 10.5V11H6.70711L6.85355 10.8536L6.5 10.5ZM4.5 10.5H4C4 10.7761 4.22386 11 4.5 11V10.5ZM4.85355 8.85355L8.85355 4.85355L8.14645 4.14645L4.14645 8.14645L4.85355 8.85355ZM8.14645 4.85355L10.1464 6.85355L10.8536 6.14645L8.85355 4.14645L8.14645 4.85355ZM10.1464 6.14645L6.14645 10.1464L6.85355 10.8536L10.8536 6.85355L10.1464 6.14645ZM6.5 10H4.5V11H6.5V10ZM5 10.5V8.5H4V10.5H5Z"
      fill={color}
    />
  {:else}
    <path
      d="M8.85355 4.14645C8.65829 3.95118 8.34171 3.95118 8.14645 4.14645L4 8.29289V10.5C4 10.7761 4.22386 11 4.5 11H6.70711L10.8536 6.85355C11.0488 6.65829 11.0488 6.34171 10.8536 6.14645L8.85355 4.14645Z"
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
@prop export let ariaLabel = 'edit small';
-->
