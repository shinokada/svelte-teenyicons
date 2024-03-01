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
  export let ariaLabel = 'gitlab';
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
      d="M0.5 8.5L7.5 14.5L14.5 8.5L12.5 0.5L10.5 6.5H4.5L2.5 0.5L0.5 8.5Z"
      stroke={color}
      stroke-linejoin="round"
    />
  {:else}
    <path
      d="M2.97436 0.341889C2.90406 0.130995 2.70297 -0.00815973 2.48083 0.000371457C2.25869 0.00890261 2.06886 0.163071 2.01495 0.378735L0.0149454 8.37874C-0.0309875 8.56247 0.0308284 8.75638 0.174621 8.87963L7.17462 14.8796C7.36187 15.0401 7.63817 15.0401 7.82541 14.8796L14.8254 8.87963C14.9692 8.75638 15.031 8.56247 14.9851 8.37874L12.9851 0.378735C12.9312 0.163071 12.7413 0.00890261 12.5192 0.000371457C12.2971 -0.00815973 12.096 0.130995 12.0257 0.341889L10.1396 6H4.8604L2.97436 0.341889Z"
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
@prop export let ariaLabel = 'gitlab';
-->
