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
  export let ariaLabel = 'html5';
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
      d="M0.5 0.5V0C0.360174 0 0.226736 0.0585498 0.132059 0.161445C0.0373814 0.264341 -0.00988477 0.40218 0.00172713 0.541523L0.5 0.5ZM14.5 0.5L14.9983 0.541523C15.0099 0.40218 14.9626 0.264341 14.8679 0.161445C14.7733 0.0585498 14.6398 0 14.5 0V0.5ZM13.5 12.5L13.6581 12.9743C13.8479 12.9111 13.9817 12.7408 13.9983 12.5415L13.5 12.5ZM7.5 14.5L7.34189 14.9743C7.44452 15.0086 7.55548 15.0086 7.65811 14.9743L7.5 14.5ZM1.5 12.5L1.00173 12.5415C1.01834 12.7408 1.15214 12.9111 1.34189 12.9743L1.5 12.5ZM4.5 3.5V3H4V3.5H4.5ZM4.5 6.5H4V7H4.5V6.5ZM10.5 6.5H11V6H10.5V6.5ZM10.5 9.5L10.6581 9.97434L11 9.86038V9.5H10.5ZM7.5 10.5L7.34189 10.9743L7.5 11.027L7.65811 10.9743L7.5 10.5ZM4.5 9.5H4V9.86038L4.34189 9.97434L4.5 9.5ZM0.5 1H14.5V0H0.5V1ZM14.0017 0.458477L13.0017 12.4585L13.9983 12.5415L14.9983 0.541523L14.0017 0.458477ZM13.3419 12.0257L7.34189 14.0257L7.65811 14.9743L13.6581 12.9743L13.3419 12.0257ZM7.65811 14.0257L1.65811 12.0257L1.34189 12.9743L7.34189 14.9743L7.65811 14.0257ZM1.99827 12.4585L0.998273 0.458477L0.00172713 0.541523L1.00173 12.5415L1.99827 12.4585ZM11 3H4.5V4H11V3ZM4 3.5V6.5H5V3.5H4ZM4.5 7H10.5V6H4.5V7ZM10 6.5V9.5H11V6.5H10ZM10.3419 9.02566L7.34189 10.0257L7.65811 10.9743L10.6581 9.97434L10.3419 9.02566ZM7.65811 10.0257L4.65811 9.02566L4.34189 9.97434L7.34189 10.9743L7.65811 10.0257ZM5 9.5V8H4V9.5H5Z"
      fill={color}
    />
  {:else}
    <path
      fill-rule="evenodd"
      clip-rule="evenodd"
      d="M0.13206 0.161445C0.226738 0.0585498 0.360176 0 0.500002 0H14.5C14.6398 0 14.7733 0.0585498 14.8679 0.161445C14.9626 0.264341 15.0099 0.40218 14.9983 0.541523L13.9983 12.5415C13.9817 12.7408 13.8479 12.9111 13.6581 12.9743L7.65812 14.9743C7.55548 15.0086 7.44452 15.0086 7.34189 14.9743L1.34189 12.9743C1.15214 12.9111 1.01834 12.7408 1.00173 12.5415L0.00172873 0.541523C-0.00988318 0.40218 0.0373829 0.264341 0.13206 0.161445ZM11 3H4V7H10V9.13962L7.5 9.97295L5 9.13962V8H4V9.86038L7.5 11.027L11 9.86038V6H5V4H11V3Z"
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
@prop export let ariaLabel = 'html5';
-->
