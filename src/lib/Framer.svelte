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
  export let ariaLabel = 'framer';
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
      d="M7.5 5.5H12.5V0.5H2.5L7.5 5.5ZM7.5 5.5H2.5V9.5L7.5 14.5V10.5H12.5L7.5 5.5Z"
      stroke={color}
      stroke-linejoin="round"
    />
  {:else}
    <path
      d="M2.03807 0.308658C2.11547 0.121821 2.29778 0 2.50001 0H12.5C12.7762 0 13 0.223858 13 0.5V5.5C13 5.77614 12.7762 6 12.5 6H8.70711L12.8536 10.1464C12.9966 10.2894 13.0393 10.5045 12.9619 10.6913C12.8845 10.8782 12.7022 11 12.5 11H8V14.5C8 14.7022 7.87818 14.8845 7.69134 14.9619C7.5045 15.0393 7.28945 14.9966 7.14645 14.8536L2.14645 9.85355C2.05268 9.75978 2 9.63261 2 9.5V5.5C2 5.22386 2.22386 5 2.5 5H6.29291L2.14646 0.853553C2.00346 0.710554 1.96068 0.495495 2.03807 0.308658Z"
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
@prop export let ariaLabel = 'framer';
-->
