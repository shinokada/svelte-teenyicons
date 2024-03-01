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
  export let ariaLabel = 'spotify';
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
      d="M14 7.5C14 11.0897 11.0903 14 7.5 14V15C11.6426 15 15 11.6419 15 7.5H14ZM7.5 14C3.90974 14 1 11.0897 1 7.5H0C0 11.6419 3.35739 15 7.5 15V14ZM1 7.5C1 3.91029 3.90974 1 7.5 1V0C3.35739 0 0 3.35806 0 7.5H1ZM7.5 1C11.0903 1 14 3.91029 14 7.5H15C15 3.35806 11.6426 0 7.5 0V1ZM3.6619 10.1162C4.64825 9.87576 5.86144 9.77072 7.05416 9.88791C8.25009 10.0054 9.38823 10.3424 10.2559 10.9525L10.8311 10.1345C9.77768 9.39382 8.45578 9.02081 7.15195 8.8927C5.84491 8.76428 4.51862 8.87807 3.42506 9.14466L3.6619 10.1162ZM3.32624 7.99237C6.772 7.38275 9.17433 7.69462 11.1649 9.12359L11.7481 8.31123C9.44985 6.66142 6.73182 6.37433 3.15202 7.00766L3.32624 7.99237ZM3.10135 5.84102C4.45435 5.36298 6.10442 5.1645 7.72549 5.29726C9.34836 5.43016 10.9042 5.8917 12.0886 6.69623L12.6505 5.86901C11.2863 4.94241 9.55125 4.44343 7.80712 4.30059C6.06118 4.15761 4.26817 4.36818 2.76821 4.89814L3.10135 5.84102Z"
      fill={color}
    />
  {:else}
    <path
      fill-rule="evenodd"
      clip-rule="evenodd"
      d="M0 7.5C0 3.35806 3.35739 0 7.5 0C11.6426 0 15 3.35806 15 7.5C15 11.6419 11.6426 15 7.5 15C3.35739 15 0 11.6419 0 7.5ZM7.72559 5.29726C6.10452 5.1645 4.45445 5.36298 3.10145 5.84102L2.76831 4.89814C4.26827 4.36818 6.06128 4.15762 7.80721 4.3006C9.55134 4.44343 11.2864 4.94242 12.6506 5.86902L12.0887 6.69623C10.9043 5.8917 9.34846 5.43017 7.72559 5.29726ZM3.32631 7.99238C6.77208 7.38276 9.1744 7.69462 11.165 9.12359L11.7482 8.31123C9.44992 6.66142 6.7319 6.37433 3.1521 7.00767L3.32631 7.99238ZM3.66189 10.1162C4.64824 9.87575 5.86143 9.77071 7.05416 9.8879C8.25008 10.0054 9.38823 10.3424 10.2559 10.9525L10.8311 10.1345C9.77767 9.39382 8.45578 9.0208 7.15194 8.8927C5.8449 8.76428 4.51861 8.87807 3.42505 9.14466L3.66189 10.1162Z"
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
@prop export let ariaLabel = 'spotify';
-->
