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
  export let ariaLabel = 'codepen';
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
      d="M7.5 0.5L7.79062 0.0931333C7.61677 -0.0310444 7.38323 -0.0310444 7.20938 0.0931333L7.5 0.5ZM14.5 5.5H15C15 5.33852 14.922 5.18699 14.7906 5.09313L14.5 5.5ZM14.5 9.5L14.7906 9.90687C14.922 9.81301 15 9.66148 15 9.5H14.5ZM7.5 14.5L7.20938 14.9069C7.38323 15.031 7.61677 15.031 7.79062 14.9069L7.5 14.5ZM0.5 9.5H0C0 9.66148 0.0779828 9.81301 0.209381 9.90687L0.5 9.5ZM0.5 5.5L0.209381 5.09313C0.0779828 5.18699 0 5.33852 0 5.5H0.5ZM7.20938 0.906867L14.2094 5.90687L14.7906 5.09313L7.79062 0.0931333L7.20938 0.906867ZM14 5.5V9.5H15V5.5H14ZM14.2094 9.09313L7.20938 14.0931L7.79062 14.9069L14.7906 9.90687L14.2094 9.09313ZM7.79062 14.0931L0.790619 9.09313L0.209381 9.90687L7.20938 14.9069L7.79062 14.0931ZM1 9.5V5.5H0V9.5H1ZM0.790619 5.90687L7.79062 0.906867L7.20938 0.0931333L0.209381 5.09313L0.790619 5.90687ZM0.790619 9.90687L7.79062 4.90687L7.20938 4.09313L0.209381 9.09313L0.790619 9.90687ZM7.20938 4.90687L14.2094 9.90687L14.7906 9.09313L7.79062 4.09313L7.20938 4.90687ZM0.209381 5.90687L7.20938 10.9069L7.79062 10.0931L0.790619 5.09313L0.209381 5.90687ZM7.79062 10.9069L14.7906 5.90687L14.2094 5.09313L7.20938 10.0931L7.79062 10.9069ZM7 0.5V4.5H8V0.5H7ZM7 10.5V14.5H8V10.5H7Z"
      fill={color}
    />
  {:else}
    <path
      fill-rule="evenodd"
      clip-rule="evenodd"
      d="M7.20938 0.0931333C7.38323 -0.0310444 7.61677 -0.0310444 7.79062 0.0931333L14.7906 5.09313C14.922 5.18699 15 5.33852 15 5.5V9.5C15 9.66148 14.922 9.81301 14.7906 9.90687L7.79062 14.9069C7.61677 15.031 7.38323 15.031 7.20938 14.9069L0.209381 9.90687C0.0779828 9.81301 0 9.66148 0 9.5V5.5C0 5.33852 0.0779828 5.18699 0.209381 5.09313L7.20938 0.0931333ZM1 6.47159L2.43977 7.5L1 8.52841V6.47159ZM1.36023 9.5L7 13.5284V10.7573L3.3 8.11445L1.36023 9.5ZM4.16023 7.5L7.5 9.88555L10.8398 7.5L7.5 5.11445L4.16023 7.5ZM8 4.24269L11.7 6.88555L13.6398 5.5L8 1.47159V4.24269ZM7 1.47159V4.24269L3.3 6.88555L1.36023 5.5L7 1.47159ZM14 6.47159L12.5602 7.5L14 8.52841V6.47159ZM13.6398 9.5L11.7 8.11445L8 10.7573V13.5284L13.6398 9.5Z"
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
@prop export let ariaLabel = 'codepen';
-->
