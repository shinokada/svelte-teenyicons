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
  export let ariaLabel = 'volume 3';
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
      d="M3.5 10.4941L3.75712 10.0653L3.63841 9.99413H3.5V10.4941ZM3.5 4.49804V4.99804H3.63841L3.75712 4.92686L3.5 4.49804ZM8.5 1.5H9C9 1.31989 8.90313 1.1537 8.74641 1.06494C8.58969 0.976173 8.39735 0.978558 8.24288 1.07118L8.5 1.5ZM8.5 13.4922L8.24288 13.921C8.39735 14.0136 8.58969 14.016 8.74641 13.9272C8.90313 13.8385 9 13.6723 9 13.4922H8.5ZM3.5 9.99413H1.5V10.9941H3.5V9.99413ZM1.5 9.99413C1.22351 9.99413 1 9.77065 1 9.49478H0C0 10.3242 0.672491 10.9941 1.5 10.9941V9.99413ZM1 9.49478V5.49739H0V9.49478H1ZM1 5.49739C1 5.22153 1.22351 4.99804 1.5 4.99804V3.99804C0.672491 3.99804 0 4.66798 0 5.49739H1ZM1.5 4.99804H3.5V3.99804H1.5V4.99804ZM3.75712 4.92686L8.75712 1.92882L8.24288 1.07118L3.24288 4.06922L3.75712 4.92686ZM8 1.5V13.4922H9V1.5H8ZM8.75712 13.0634L3.75712 10.0653L3.24288 10.923L8.24288 13.921L8.75712 13.0634ZM10 6V9H11V6H10ZM12 4V11H13V4H12ZM14 2V13H15V2H14Z"
      fill={color}
    />
  {:else}
    <path
      d="M9 1.5C9 1.31989 8.90313 1.1537 8.74641 1.06494C8.58969 0.976173 8.39735 0.978558 8.24288 1.07118L3.36159 3.99804H1.5C0.672491 3.99804 0 4.66798 0 5.49739V9.49479C0 10.3242 0.672491 10.9941 1.5 10.9941H3.36159L8.24288 13.921C8.39735 14.0136 8.58969 14.016 8.74641 13.9272C8.90313 13.8385 9 13.6723 9 13.4922V1.5Z"
      fill={color}
    /> <path d="M14 2V13H15V2H14Z" fill={color} /> <path d="M12 4V11H13V4H12Z" fill={color} />
    <path d="M10 6V9H11V6H10Z" fill={color} />
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
@prop export let ariaLabel = 'volume 3';
-->
