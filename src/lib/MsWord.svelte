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
  export let ariaLabel = 'ms word';
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
      d="M3.5 9.5L3.01493 9.62127C3.06293 9.81327 3.21966 9.95889 3.41466 9.99266C3.60967 10.0264 3.80625 9.94202 3.91603 9.77735L3.5 9.5ZM4.5 8L4.91603 7.72265C4.82329 7.58355 4.66718 7.5 4.5 7.5C4.33282 7.5 4.17671 7.58355 4.08397 7.72265L4.5 8ZM5.5 9.5L5.08397 9.77735C5.19375 9.94202 5.39033 10.0264 5.58534 9.99266C5.78034 9.95889 5.93707 9.81327 5.98507 9.62127L5.5 9.5ZM1.5 4H7.5V3H1.5V4ZM8 4.5V10.5H9V4.5H8ZM7.5 11H1.5V12H7.5V11ZM1 10.5V4.5H0V10.5H1ZM1.5 11C1.22386 11 1 10.7761 1 10.5H0C0 11.3284 0.671573 12 1.5 12V11ZM8 10.5C8 10.7761 7.77614 11 7.5 11V12C8.32843 12 9 11.3284 9 10.5H8ZM7.5 4C7.77614 4 8 4.22386 8 4.5H9C9 3.67157 8.32843 3 7.5 3V4ZM1.5 3C0.671573 3 0 3.67157 0 4.5H1C1 4.22386 1.22386 4 1.5 4V3ZM2.01493 5.62127L3.01493 9.62127L3.98507 9.37873L2.98507 5.37873L2.01493 5.62127ZM3.91603 9.77735L4.91603 8.27735L4.08397 7.72265L3.08397 9.22265L3.91603 9.77735ZM4.08397 8.27735L5.08397 9.77735L5.91603 9.22265L4.91603 7.72265L4.08397 8.27735ZM5.98507 9.62127L6.98507 5.62127L6.01493 5.37873L5.01493 9.37873L5.98507 9.62127ZM3 3.5V1.5H2V3.5H3ZM3.5 1H13.5V0H3.5V1ZM14 1.5V13.5H15V1.5H14ZM13.5 14H3.5V15H13.5V14ZM3 13.5V11.5H2V13.5H3ZM3.5 14C3.22386 14 3 13.7761 3 13.5H2C2 14.3284 2.67157 15 3.5 15V14ZM14 13.5C14 13.7761 13.7761 14 13.5 14V15C14.3284 15 15 14.3284 15 13.5H14ZM13.5 1C13.7761 1 14 1.22386 14 1.5H15C15 0.671573 14.3284 0 13.5 0V1ZM3 1.5C3 1.22386 3.22386 1 3.5 1V0C2.67157 0 2 0.671573 2 1.5H3Z"
      fill={color}
    />
  {:else}
    <path
      d="M2.01489 5.62126L3.01489 9.62126C3.06289 9.81326 3.21962 9.95888 3.41463 9.99265C3.60963 10.0264 3.80621 9.94201 3.91599 9.77734L4.49996 8.90138L5.08394 9.77734C5.19372 9.94201 5.3903 10.0264 5.5853 9.99265C5.7803 9.95888 5.93704 9.81326 5.98503 9.62126L6.98503 5.62126L6.01489 5.37872L5.28902 8.28219L4.91599 7.72264C4.82326 7.58354 4.66714 7.49999 4.49996 7.49999C4.33279 7.49999 4.17667 7.58354 4.08394 7.72264L3.7109 8.28219L2.98503 5.37872L2.01489 5.62126Z"
      fill={color}
    />
    <path
      fill-rule="evenodd"
      clip-rule="evenodd"
      d="M3.5 0C2.67157 0 2 0.671573 2 1.5V3H1.5C0.671573 3 0 3.67157 0 4.5V10.5C0 11.3284 0.671573 12 1.5 12H2V13.5C2 14.3284 2.67157 15 3.5 15H13.5C14.3284 15 15 14.3284 15 13.5V1.5C15 0.671573 14.3284 0 13.5 0H3.5ZM1.5 4C1.22386 4 1 4.22386 1 4.5V10.5C1 10.7761 1.22386 11 1.5 11H7.5C7.77614 11 8 10.7761 8 10.5V4.5C8 4.22386 7.77614 4 7.5 4H1.5Z"
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
@prop export let ariaLabel = 'ms word';
-->
