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
  export let ariaLabel = 'chrome';
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
      d="M13.5 5C13.7761 5 14 4.77614 14 4.5C14 4.22386 13.7761 4 13.5 4V5ZM2.96423 2.81431C2.86168 2.55791 2.57069 2.43321 2.3143 2.53576C2.05791 2.63832 1.9332 2.9293 2.03576 3.1857L2.96423 2.81431ZM14 7.5C14 11.0903 11.0903 14 7.5 14V15C11.6426 15 15 11.6426 15 7.5H14ZM7.5 14C3.90971 14 1 11.0903 1 7.5H0C0 11.6426 3.35742 15 7.5 15V14ZM1 7.5C1 3.90971 3.90971 1 7.5 1V0C3.35742 0 0 3.35742 0 7.5H1ZM7.5 1C11.0903 1 14 3.90971 14 7.5H15C15 3.35742 11.6426 0 7.5 0V1ZM7.5 5H13.5V4H7.5V5ZM4.96423 7.81431L2.96423 2.81431L2.03576 3.1857L4.03576 8.1857L4.96423 7.81431ZM9.24901 9.30131L5.59901 14.2013L6.40097 14.7987L10.051 9.89869L9.24901 9.30131ZM7.5 10C6.11929 10 5 8.88071 5 7.5H4C4 9.433 5.567 11 7.5 11V10ZM10 7.5C10 8.88071 8.88071 10 7.5 10V11C9.433 11 11 9.433 11 7.5H10ZM7.5 5C8.88071 5 10 6.11929 10 7.5H11C11 5.567 9.433 4 7.5 4V5ZM7.5 4C5.567 4 4 5.567 4 7.5H5C5 6.11929 6.11929 5 7.5 5V4Z"
      fill={color}
    />
  {:else}
    <path
      d="M2.50278 1.90694C3.82927 0.720967 5.58034 0 7.5 0C10.3784 0 12.8778 1.62097 14.1351 4H7.5C6.0459 4 4.79892 4.88673 4.27029 6.14895L2.50278 1.90694Z"
      fill={color}
    />
    <path
      d="M1.74548 2.68942C0.655856 3.99152 0 5.66907 0 7.5C0 10.8241 2.16179 13.6427 5.15637 14.6267L7.96726 10.9691C7.8144 10.9895 7.65843 11 7.5 11C5.83646 11 4.44398 9.83942 4.08809 8.28377C4.06875 8.25563 4.052 8.22508 4.03835 8.1923L1.74548 2.68942Z"
      fill={color}
    />
    <path
      d="M6.2149 14.8904C6.63245 14.9624 7.06184 15 7.5 15C11.6426 15 15 11.6426 15 7.5C15 6.62148 14.849 5.77828 14.5715 4.99492C14.5482 4.99827 14.5243 5 14.5 5H9.94949C10.5978 5.63526 11 6.52066 11 7.5C11 8.42321 10.6426 9.26293 10.0585 9.88832C10.0546 9.89383 10.0506 9.89928 10.0465 9.90468L6.2149 14.8904Z"
      fill={color}
    />
    <path
      d="M5 7.5C5 6.11929 6.11929 5 7.5 5C8.88071 5 10 6.11929 10 7.5C10 8.88071 8.88071 10 7.5 10C6.11929 10 5 8.88071 5 7.5Z"
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
@prop export let ariaLabel = 'chrome';
-->
