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
  export let ariaLabel = 'code';
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
      d="M10.1464 10.1464L9.79289 10.5L10.5 11.2071L10.8536 10.8536L10.1464 10.1464ZM13.5 7.5L13.8536 7.85355L14.2071 7.5L13.8536 7.14645L13.5 7.5ZM10.8536 4.14645L10.5 3.79289L9.79289 4.5L10.1464 4.85355L10.8536 4.14645ZM4.14645 10.8536L4.5 11.2071L5.20711 10.5L4.85355 10.1464L4.14645 10.8536ZM1.5 7.5L1.14645 7.14645L0.792893 7.5L1.14645 7.85355L1.5 7.5ZM4.85355 4.85355L5.20711 4.5L4.5 3.79289L4.14645 4.14645L4.85355 4.85355ZM10.8536 10.8536L13.8536 7.85355L13.1464 7.14645L10.1464 10.1464L10.8536 10.8536ZM13.8536 7.14645L10.8536 4.14645L10.1464 4.85355L13.1464 7.85355L13.8536 7.14645ZM4.85355 10.1464L1.85355 7.14645L1.14645 7.85355L4.14645 10.8536L4.85355 10.1464ZM1.85355 7.85355L4.85355 4.85355L4.14645 4.14645L1.14645 7.14645L1.85355 7.85355ZM8.0068 1.4178L6.0068 13.4178L6.9932 13.5822L8.9932 1.5822L8.0068 1.4178Z"
      fill={color}
    />
  {:else}
    <path
      fill-rule="evenodd"
      clip-rule="evenodd"
      d="M6.0068 13.4178L8.0068 1.4178L8.9932 1.5822L6.9932 13.5822L6.0068 13.4178ZM5.20711 4.5L2.20711 7.5L5.20711 10.5L4.5 11.2071L0.792892 7.5L4.5 3.79289L5.20711 4.5ZM10.5 3.79289L14.2071 7.5L10.5 11.2071L9.79289 10.5L12.7929 7.5L9.79289 4.5L10.5 3.79289Z"
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
@prop export let ariaLabel = 'code';
-->
