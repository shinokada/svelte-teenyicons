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
  export let ariaLabel = 'eslint';
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
      d="M0.5 7.5L0.0527864 7.27639C-0.0175955 7.41716 -0.0175955 7.58284 0.0527864 7.72361L0.5 7.5ZM3.5 1.5V1C3.31061 1 3.13748 1.107 3.05279 1.27639L3.5 1.5ZM11.5 1.5L11.9472 1.27639C11.8625 1.107 11.6894 1 11.5 1V1.5ZM14.5 7.5L14.9472 7.72361C15.0176 7.58284 15.0176 7.41716 14.9472 7.27639L14.5 7.5ZM11.5 13.5V14C11.6894 14 11.8625 13.893 11.9472 13.7236L11.5 13.5ZM3.5 13.5L3.05279 13.7236C3.13748 13.893 3.31061 14 3.5 14V13.5ZM7.5 4L7.77735 3.58397L7.5 3.39907L7.22265 3.58397L7.5 4ZM4.5 6L4.22265 5.58397L4 5.73241V6H4.5ZM4.5 9H4V9.26759L4.22265 9.41603L4.5 9ZM7.5 11L7.22265 11.416L7.5 11.6009L7.77735 11.416L7.5 11ZM10.5 9L10.7774 9.41603L11 9.26759V9H10.5ZM10.5 6H11V5.73241L10.7774 5.58397L10.5 6ZM0.947214 7.72361L3.94721 1.72361L3.05279 1.27639L0.0527864 7.27639L0.947214 7.72361ZM3.5 2H11.5V1H3.5V2ZM11.0528 1.72361L14.0528 7.72361L14.9472 7.27639L11.9472 1.27639L11.0528 1.72361ZM14.0528 7.27639L11.0528 13.2764L11.9472 13.7236L14.9472 7.72361L14.0528 7.27639ZM11.5 13H3.5V14H11.5V13ZM3.94721 13.2764L0.947214 7.27639L0.0527864 7.72361L3.05279 13.7236L3.94721 13.2764ZM7.22265 3.58397L4.22265 5.58397L4.77735 6.41603L7.77735 4.41603L7.22265 3.58397ZM4 6V9H5V6H4ZM4.22265 9.41603L7.22265 11.416L7.77735 10.584L4.77735 8.58397L4.22265 9.41603ZM7.77735 11.416L10.7774 9.41603L10.2226 8.58397L7.22265 10.584L7.77735 11.416ZM11 9V6H10V9H11ZM10.7774 5.58397L7.77735 3.58397L7.22265 4.41603L10.2226 6.41603L10.7774 5.58397Z"
      fill={color}
    />
  {:else}
    <path d="M5 8.73238V6.26756L7.5 4.6009L10 6.26756V8.73238L7.5 10.399L5 8.73238Z" fill={color} />
    <path
      fill-rule="evenodd"
      clip-rule="evenodd"
      d="M3.05279 1.27639C3.13748 1.107 3.31061 1 3.5 1H11.5C11.6894 1 11.8625 1.107 11.9472 1.27639L14.9472 7.27639C15.0176 7.41716 15.0176 7.58284 14.9472 7.72361L11.9472 13.7236C11.8625 13.893 11.6894 14 11.5 14H3.5C3.31061 14 3.13748 13.893 3.05279 13.7236L0.0527864 7.72361C-0.0175955 7.58284 -0.0175955 7.41716 0.0527864 7.27639L3.05279 1.27639ZM11 5.73238L7.5 3.39905L4 5.73238V9.26756L7.5 11.6009L11 9.26756V5.73238Z"
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
@prop export let ariaLabel = 'eslint';
-->
