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
  export let ariaLabel = 'ethereum';
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
      d="M7.5 0.5L7.88411 0.179908C7.78911 0.0659115 7.64839 0 7.5 0C7.35161 0 7.21089 0.0659115 7.11589 0.179908L7.5 0.5ZM2.5 6.5L2.11589 6.17991C1.97761 6.34585 1.96152 6.58183 2.076 6.765L2.5 6.5ZM7.5 14.5L7.076 14.765C7.16737 14.9112 7.3276 15 7.5 15C7.6724 15 7.83263 14.9112 7.924 14.765L7.5 14.5ZM12.5 6.5L12.924 6.765C13.0385 6.58183 13.0224 6.34585 12.8841 6.17991L12.5 6.5ZM7.5 4.5L7.6857 4.03576L7.5 3.96148L7.3143 4.03576L7.5 4.5ZM7.11589 0.179908L2.11589 6.17991L2.88411 6.82009L7.88411 0.820092L7.11589 0.179908ZM2.076 6.765L7.076 14.765L7.924 14.235L2.924 6.235L2.076 6.765ZM7.924 14.765L12.924 6.765L12.076 6.235L7.076 14.235L7.924 14.765ZM12.8841 6.17991L7.88411 0.179908L7.11589 0.820092L12.1159 6.82009L12.8841 6.17991ZM2.6857 6.96424L7.6857 4.96424L7.3143 4.03576L2.3143 6.03576L2.6857 6.96424ZM7.3143 4.96424L12.3143 6.96424L12.6857 6.03576L7.6857 4.03576L7.3143 4.96424Z"
      fill={color}
    />
  {:else}
    <path
      fill-rule="evenodd"
      clip-rule="evenodd"
      d="M7.5 0C7.64839 0 7.78911 0.0659115 7.88411 0.179908L12.8841 6.17991C13.0224 6.34585 13.0385 6.58183 12.924 6.765L7.924 14.765C7.83263 14.9112 7.67239 15 7.5 15C7.3276 15 7.16737 14.9112 7.076 14.765L2.076 6.765C1.96152 6.58183 1.97761 6.34585 2.11589 6.17991L7.11589 0.179908C7.21089 0.0659115 7.35161 0 7.5 0ZM3.24096 6.74213L7.5 5.03852L11.759 6.74213L7.5 13.5566L3.24096 6.74213ZM10.8506 5.30171L7.5 3.96148L4.14943 5.30171L7.5 1.28102L10.8506 5.30171Z"
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
@prop export let ariaLabel = 'ethereum';
-->
