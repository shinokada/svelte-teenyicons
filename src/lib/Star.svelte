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
  export let ariaLabel = 'star';
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
      d="M7.5 12.0405L3.17354 14.3151L4 9.4973L0.5 6.08562L5.33677 5.38324L7.5 1L9.66323 5.38324L14.5 6.08562L11 9.4973L11.8265 14.3151L7.5 12.0405Z"
      stroke={color}
      stroke-linecap="round"
      stroke-linejoin="round"
    />
  {:else}
    <path
      d="M7.94838 0.778719C7.86415 0.60805 7.69034 0.5 7.50001 0.5C7.30969 0.5 7.13587 0.60805 7.05165 0.778719L5.00476 4.92621L0.42816 5.59081C0.239806 5.61816 0.0833166 5.75008 0.0244934 5.93109C-0.0343298 6.1121 0.0147161 6.31081 0.151008 6.44366L3.46277 9.67185L2.68076 14.2306C2.64858 14.4182 2.72569 14.6078 2.87966 14.7196C3.03364 14.8315 3.23778 14.8463 3.40624 14.7577L7.50001 12.6054L11.5938 14.7577C11.7623 14.8463 11.9664 14.8315 12.1204 14.7196C12.2743 14.6078 12.3515 14.4182 12.3193 14.2306L11.5373 9.67185L14.849 6.44366C14.9853 6.31081 15.0344 6.1121 14.9755 5.93109C14.9167 5.75008 14.7602 5.61816 14.5719 5.59081L9.99527 4.92621L7.94838 0.778719Z"
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
@prop export let ariaLabel = 'star';
-->
