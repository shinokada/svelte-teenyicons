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
  export let ariaLabel = 'bitcoin';
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
      d="M3.5 1.5H8.5C10.1569 1.5 11.5 2.84315 11.5 4.5C11.5 6.15685 10.1569 7.5 8.5 7.5H3.5M3.5 1.5V7.5M3.5 1.5H2M3.5 1.5V0M3.5 7.5H9.5C11.1569 7.5 12.5 8.84315 12.5 10.5C12.5 12.1569 11.1569 13.5 9.5 13.5H3.5M3.5 7.5V13.5M3.5 7.5H2M3.5 13.5H2M3.5 13.5V15M7.5 0V1.5M7.5 13.5V15"
      stroke={color}
    />
  {:else}
    <path
      fill-rule="evenodd"
      clip-rule="evenodd"
      d="M3 1V0H4V1H7V0H8V1H8.5C10.433 1 12 2.567 12 4.5C12 5.59515 11.497 6.57282 10.7095 7.2146C12.0464 7.70695 13 8.99212 13 10.5C13 12.433 11.433 14 9.5 14H8V15H7V14H4V15H3V14H2V13H3V8H2V7H3V2H2V1H3ZM4 2V7H8.5C9.88071 7 11 5.88071 11 4.5C11 3.11929 9.88071 2 8.5 2H4ZM4 8H9.5C10.8807 8 12 9.11929 12 10.5C12 11.8807 10.8807 13 9.5 13H4V8Z"
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
@prop export let ariaLabel = 'bitcoin';
-->
