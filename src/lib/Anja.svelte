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
  export let ariaLabel = 'anja';
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
      d="M9.00746 4.4005L9.04072 3.9016L9.00746 4.4005ZM2.95478 8.13786L2.49374 7.94437L2.95478 8.13786ZM7.5 14C5.87329 14 4.39916 13.042 3.73849 11.5555L2.82468 11.9616C3.64585 13.8093 5.4781 15 7.5 15V14ZM11.2615 11.5555C10.6008 13.042 9.12671 14 7.5 14V15C9.5219 15 11.3541 13.8093 12.1753 11.9616L11.2615 11.5555ZM2 15V6H1V15H2ZM7.5 1C10.5376 1 13 3.46243 13 6.5H14C14 2.91015 11.0899 0 7.5 0V1ZM2 6.5C2 3.46243 4.46243 1 7.5 1V0C3.91015 0 1 2.91015 1 6.5H2ZM13 6.5V15H14V6.5H13ZM8.9742 4.89939L10.4667 4.99889L10.5333 4.00111L9.04072 3.9016L8.9742 4.89939ZM11 4.5V3H10V4.5H11ZM3.41582 8.33136C4.32054 6.17573 6.51869 4.73569 8.9742 4.89939L9.04072 3.9016C6.14682 3.70868 3.55895 5.40634 2.49374 7.94437L3.41582 8.33136ZM10.1464 4.85355C10.6164 5.32348 11.4761 6.3438 11.8352 8.19581L12.8169 8.00545C12.4098 5.90613 11.4221 4.71504 10.8536 4.14645L10.1464 4.85355ZM6.5 13H8V12H6.5V13ZM8 13C9.10457 13 10 12.1046 10 11H9C9 11.5523 8.55228 12 8 12V13ZM12.5 9H10.5V10H12.5V9ZM8.5 8H12V7H8.5V8ZM3.5 8H6.5V7H3.5V8ZM6.5 8H8.5V7H6.5V8ZM4.5 9H2.5V10H4.5V9ZM6 7.5C6 8.32843 5.32843 9 4.5 9V10C5.88071 10 7 8.88071 7 7.5H6ZM10.5 9C9.67157 9 9 8.32843 9 7.5H8C8 8.88071 9.11929 10 10.5 10V9ZM3.73849 11.5555C3.2427 10.44 3.00886 9.30102 3.41582 8.33136L2.49374 7.94437C1.92348 9.30312 2.29491 10.7696 2.82468 11.9616L3.73849 11.5555ZM12.1753 11.9616C12.7043 10.7715 13.085 9.38793 12.8169 8.00545L11.8352 8.19581C12.0466 9.2858 11.7554 10.4442 11.2615 11.5555L12.1753 11.9616Z"
      fill={color}
    />
  {:else}
    <path
      d="M8 13C9.10457 13 10 12.1046 10 11H9C9 11.5523 8.55228 12 8 12H6.5V13H8Z"
      fill={color}
    />
    <path
      fill-rule="evenodd"
      clip-rule="evenodd"
      d="M7.5 15C7.31717 15 7.1359 14.9903 6.95678 14.9712L7 15H1V6H1.01894C1.27426 2.64378 4.07839 0 7.5 0C11.0899 0 14 2.91015 14 6.5V15H7.5ZM8.9742 4.89939L10.2747 4.98609C10.632 5.36762 11.1319 6.01019 11.5016 7H4.20723C5.31862 5.61087 7.06894 4.77237 8.9742 4.89939ZM9.08535 8H11.7947C11.8088 8.06421 11.8223 8.12948 11.8352 8.19581C11.8865 8.46039 11.9082 8.72901 11.9046 9H10.5C9.84689 9 9.29127 8.5826 9.08535 8ZM10.5 10H11.7859C11.6738 10.521 11.4892 11.0432 11.2615 11.5555C10.6008 13.042 9.12671 14 7.5 14C5.87329 14 4.39916 13.042 3.73849 11.5555C3.50742 11.0356 3.33324 10.5106 3.25433 10H4.5C5.70948 10 6.71836 9.14112 6.94999 8H8.05001C8.28164 9.14112 9.29052 10 10.5 10ZM4.5 9H3.23539C3.26673 8.77018 3.32549 8.5466 3.41582 8.33136C3.46302 8.21892 3.51373 8.10842 3.56781 8H5.91465C5.70873 8.5826 5.15311 9 4.5 9Z"
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
@prop export let ariaLabel = 'anja';
-->
