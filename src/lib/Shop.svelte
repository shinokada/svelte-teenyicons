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
  export let ariaLabel = 'shop';
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
      d="M1.5 2.5V2C1.26166 2 1.05645 2.16823 1.00971 2.40194L1.5 2.5ZM13.5 2.5L13.9903 2.40194C13.9435 2.16823 13.7383 2 13.5 2V2.5ZM14.5 7.5V8C14.6498 8 14.7917 7.93284 14.8867 7.81699C14.9816 7.70115 15.0197 7.54883 14.9903 7.40194L14.5 7.5ZM0.5 7.5L0.00970966 7.40194C-0.0196679 7.54883 0.0183596 7.70115 0.113329 7.81699C0.208298 7.93284 0.350203 8 0.5 8V7.5ZM3.5 10.5H3V11H3.5V10.5ZM11.5 10.5V11H12V10.5H11.5ZM0 15H15V14H0V15ZM1 7.5V14.5H2V7.5H1ZM13 7.5V14.5H14V7.5H13ZM1.5 3H13.5V2H1.5V3ZM13.0097 2.59806L14.0097 7.59806L14.9903 7.40194L13.9903 2.40194L13.0097 2.59806ZM14.5 7H0.5V8H14.5V7ZM0.99029 7.59806L1.99029 2.59806L1.00971 2.40194L0.00970966 7.40194L0.99029 7.59806ZM1 1H14V0H1V1ZM3 7.5V10.5H4V7.5H3ZM3.5 11H11.5V10H3.5V11ZM12 10.5V7.5H11V10.5H12Z"
      fill={color}
    />
  {:else}
    <path d="M14 1H1V0H14V1Z" fill={color} />
    <path
      d="M1.00971 2.40194C1.05646 2.16823 1.26166 2 1.5 2H13.5C13.7383 2 13.9436 2.16823 13.9903 2.40194L14.9903 7.40194C15.0197 7.54883 14.9816 7.70115 14.8867 7.81699C14.7917 7.93284 14.6498 8 14.5 8H0.500004C0.350208 8 0.208303 7.93284 0.113333 7.81699C0.0183639 7.70115 -0.0196636 7.54883 0.00971396 7.40194L1.00971 2.40194Z"
      fill={color}
    /> <path d="M1 9V14H1.46883e-10V15H15V14H14V9H12V11H3V9H1Z" fill={color} />
    <path d="M4 9H11V10H4V9Z" fill={color} />
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
@prop export let ariaLabel = 'shop';
-->
