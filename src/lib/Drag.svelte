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
  export let ariaLabel = 'drag';
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
      d="M7.5 7.5L7.63736 7.01924C7.46276 6.96935 7.27485 7.01805 7.14645 7.14645C7.01805 7.27485 6.96935 7.46276 7.01924 7.63736L7.5 7.5ZM9.5 14.5L9.01924 14.6374C9.07736 14.8408 9.25723 14.9856 9.46837 14.999C9.67952 15.0124 9.87623 14.8914 9.95957 14.697L9.5 14.5ZM14.5 9.5L14.697 9.95957C14.8914 9.87623 15.0124 9.67952 14.999 9.46837C14.9856 9.25723 14.8408 9.07736 14.6374 9.01924L14.5 9.5ZM11 11L10.803 10.5404C10.685 10.591 10.591 10.685 10.5404 10.803L11 11ZM3.5 3.5V3H3V3.5H3.5ZM13.5 3.5H14V3H13.5V3.5ZM3.5 13.5H3V14H3.5V13.5ZM0 1H1V0H0V1ZM4 1H5V0H4V1ZM8 1H9V0H8V1ZM0 5H1V4H0V5ZM0 9H1V8H0V9ZM7.01924 7.63736L9.01924 14.6374L9.98076 14.3626L7.98076 7.36264L7.01924 7.63736ZM14.6374 9.01924L7.63736 7.01924L7.36264 7.98076L14.3626 9.98076L14.6374 9.01924ZM9.95957 14.697L11.4596 11.197L10.5404 10.803L9.04043 14.303L9.95957 14.697ZM11.197 11.4596L14.697 9.95957L14.303 9.04043L10.803 10.5404L11.197 11.4596ZM3.5 4H13.5V3H3.5V4ZM13 3.5V7H14V3.5H13ZM3 3.5V13.5H4V3.5H3ZM3.5 14H7V13H3.5V14Z"
      fill={color}
    />
  {:else}
    <path
      fill-rule="evenodd"
      clip-rule="evenodd"
      d="M1 1H0V0H1V1ZM5 1H4V0H5V1ZM9 1H8V0H9V1ZM3 3H14V7H13V4H4V13H7V14H3V3ZM1 5H0V4H1V5ZM7.14645 7.14645C7.27485 7.01805 7.46276 6.96935 7.63736 7.01924L14.6374 9.01924C14.8408 9.07736 14.9856 9.25723 14.999 9.46837C15.0124 9.67952 14.8914 9.87623 14.697 9.95957L11.3808 11.3808L9.95957 14.697C9.87623 14.8914 9.67952 15.0124 9.46837 14.999C9.25723 14.9856 9.07736 14.8408 9.01924 14.6374L7.01924 7.63736C6.96935 7.46276 7.01805 7.27485 7.14645 7.14645ZM8.22801 8.22801L9.59441 13.0104L10.5404 10.803C10.591 10.685 10.685 10.591 10.803 10.5404L13.0104 9.59441L8.22801 8.22801ZM1 9H0V8H1V9Z"
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
@prop export let ariaLabel = 'drag';
-->
