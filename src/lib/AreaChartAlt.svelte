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
  export let ariaLabel = 'area chart alt';
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
      d="M0.5 14.5H0V15H0.5V14.5ZM2 11.5V12H3V11.5H2ZM15 2.5V2H14V2.5H15ZM0 0V14.5H1V0H0ZM0.5 15H15V14H0.5V15ZM3 11.5C3 10.0456 3.24378 8.6201 3.70691 7.57807C4.17757 6.51908 4.79814 6 5.5 6V5C4.20186 5 3.32243 5.98092 2.79309 7.17193C2.25622 8.3799 2 9.95441 2 11.5H3ZM5.5 6C5.82076 6 6.14191 6.15761 6.50461 6.4924C6.87081 6.83043 7.21786 7.29048 7.6 7.8C7.96786 8.29048 8.37081 8.83043 8.81711 9.2424C9.26691 9.65761 9.82076 10 10.5 10V9C10.1792 9 9.85809 8.84239 9.49539 8.5076C9.12919 8.16957 8.78214 7.70952 8.4 7.2C8.03214 6.70952 7.62919 6.16957 7.18289 5.7576C6.73309 5.34239 6.17924 5 5.5 5V6ZM10.5 10C11.7232 10 12.8626 9.23726 13.6727 7.9545C14.4853 6.66802 15 4.8191 15 2.5H14C14 4.6809 13.5147 6.33198 12.8273 7.4205C12.1374 8.51274 11.2768 9 10.5 9V10Z"
      fill={color}
    />
  {:else}
    <path
      d="M1 0H0V15H15V14.5063C15 14.5042 15 14.5021 15 14.5V2.5C15 2.22386 14.7762 2 14.5 2C14.2239 2 14 2.22386 14 2.5C14 4.6809 13.5148 6.33198 12.8273 7.4205C12.1375 8.51274 11.2769 9 10.5 9C10.1793 9 9.85813 8.84239 9.49543 8.5076C9.12923 8.16957 8.78218 7.70952 8.40004 7.2L8.38432 7.17904C8.02071 6.69418 7.62288 6.1637 7.18293 5.7576C6.73313 5.34239 6.17928 5 5.50004 5C4.2019 5 3.32247 5.98092 2.79313 7.17193C2.25626 8.3799 2.00004 9.95441 2.00004 11.5V11.6972C2.00004 12.5394 1.63043 13.3327 1 13.8738V0Z"
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
@prop export let ariaLabel = 'area chart alt';
-->
