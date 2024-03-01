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
  export let ariaLabel = 'roller';
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
      d="M13.0494 7.91444L12.9121 7.43368L13.0494 7.91444ZM8.22528 9.29278L8.36264 9.77354L8.36264 9.77354L8.22528 9.29278ZM5.5 11.5V11C5.22386 11 5 11.2239 5 11.5H5.5ZM9.5 11.5H10C10 11.2239 9.77614 11 9.5 11V11.5ZM9.5 14.5V15C9.77614 15 10 14.7761 10 14.5H9.5ZM5.5 14.5H5C5 14.7761 5.22386 15 5.5 15V14.5ZM1.5 1H11.5V0H1.5V1ZM12 1.5V3.5H13V1.5H12ZM11.5 4H1.5V5H11.5V4ZM1 3.5V1.5H0V3.5H1ZM1.5 4C1.22386 4 1 3.77614 1 3.5H0C0 4.32843 0.671573 5 1.5 5V4ZM12 3.5C12 3.77614 11.7761 4 11.5 4V5C12.3284 5 13 4.32843 13 3.5H12ZM11.5 1C11.7761 1 12 1.22386 12 1.5H13C13 0.671573 12.3284 0 11.5 0V1ZM1.5 0C0.671573 0 0 0.671573 0 1.5H1C1 1.22386 1.22386 1 1.5 1V0ZM14 4.5V5.9914H15V4.5H14ZM12.9121 7.43368L8.08792 8.81202L8.36264 9.77354L13.1868 8.39521L12.9121 7.43368ZM7 10.2543V11.5H8V10.2543H7ZM8.08792 8.81202C7.44397 8.996 7 9.58458 7 10.2543H8C8 10.0311 8.14799 9.83487 8.36264 9.77354L8.08792 8.81202ZM14 5.9914C14 6.66112 13.556 7.2497 12.9121 7.43368L13.1868 8.39521C14.2601 8.08856 15 7.1076 15 5.9914H14ZM12.5 3C13.3284 3 14 3.67157 14 4.5H15C15 3.11929 13.8807 2 12.5 2V3ZM5.5 12H9.5V11H5.5V12ZM9 11.5V14.5H10V11.5H9ZM9.5 14H5.5V15H9.5V14ZM6 14.5V11.5H5V14.5H6Z"
      fill={color}
    />
  {:else}
    <path
      d="M0 1.5C0 0.671573 0.671573 0 1.5 0H11.5C12.3284 0 13 0.671573 13 1.5V2.05001C14.1411 2.28164 15 3.29052 15 4.5V5.9914C15 7.1076 14.2601 8.08856 13.1868 8.39521L8.36264 9.77354C8.14799 9.83487 8 10.0311 8 10.2543V11H9.5C9.77614 11 10 11.2239 10 11.5V14.5C10 14.7761 9.77614 15 9.5 15H5.5C5.22386 15 5 14.7761 5 14.5V11.5C5 11.2239 5.22386 11 5.5 11H7V10.2543C7 9.58458 7.44397 8.996 8.08792 8.81202L12.9121 7.43368C13.556 7.2497 14 6.66112 14 5.9914V4.5C14 3.84689 13.5826 3.29127 13 3.08535V3.5C13 4.32843 12.3284 5 11.5 5H1.5C0.671572 5 0 4.32843 0 3.5V1.5Z"
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
@prop export let ariaLabel = 'roller';
-->
