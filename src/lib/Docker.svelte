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
  export let ariaLabel = 'docker';
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
      d="M0.5 5.5V5H0V5.5H0.5ZM2.5 3.5V3H2V3.5H2.5ZM6.5 1.5V1H6V1.5H6.5ZM8.5 1.5H9V1H8.5V1.5ZM12.5 7.5H12V8H12.5V7.5ZM1 7.5V5.5H0V7.5H1ZM3 7.5V3.5H2V7.5H3ZM2.5 4H8.5V3H2.5V4ZM8 3.5V7.5H9V3.5H8ZM5 7.5V3.5H4V7.5H5ZM7 7.5V1.5H6V7.5H7ZM6.5 2H8.5V1H6.5V2ZM8 1.5V3.5H9V1.5H8ZM13.7361 10H15V9H13.7361V10ZM10 5V5.5H11V5H10ZM12 6.5V7.5H13V6.5H12ZM12.5 8H13.5V7H12.5V8ZM14 8.5V9.5H15V8.5H14ZM13.5 8C13.7761 8 14 8.22386 14 8.5H15C15 7.67157 14.3284 7 13.5 7V8ZM11.5 6C11.7761 6 12 6.22386 12 6.5H13C13 5.67157 12.3284 5 11.5 5V6ZM3 10H4V9H3V10ZM8.5 7H0.5V8H8.5V7ZM0 7.5V8.5H1V7.5H0ZM5.5 14H6.02786V13H5.5V14ZM6.02786 14C8.51265 14 10.8164 12.8096 12.2585 10.8496L11.4531 10.257C10.1974 11.9636 8.19126 13 6.02786 13V14ZM0 8.5C0 11.5376 2.46243 14 5.5 14V13C3.01472 13 1 10.9853 1 8.5H0ZM0.5 6H11.5V5H0.5V6ZM10 5.5C10 6.32843 9.32843 7 8.5 7V8C9.88071 8 11 6.88071 11 5.5H10ZM13.7361 9C12.7762 9 11.9673 9.55817 11.4531 10.257L12.2585 10.8496C12.6423 10.3281 13.1808 10 13.7361 10V9Z"
      fill={color}
    />
  {:else}
    <path
      fill-rule="evenodd"
      clip-rule="evenodd"
      d="M9 1H6V3H2V5H0V8.5C0 11.5376 2.46243 14 5.5 14H6.02786C8.85368 14 11.4456 12.4603 12.802 10H15V8.5C15 7.67157 14.3284 7 13.5 7H13V6.5C13 5.67157 12.3284 5 11.5 5H9V1ZM1 7H2V6H1V7ZM3 7H4V6H3V7ZM5 7H6V6H5V7ZM7 7H8V6H7V7ZM9 7H10V6H9V7ZM8 3V2H7V3H8ZM6 4H5V5H6V4ZM7 5V4H8V5H7ZM4 5V4H3V5H4ZM3 10H4V9H3V10Z"
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
@prop export let ariaLabel = 'docker';
-->
