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
  export let ariaLabel = 'diamond';
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
      d="M7.5 14.5L7.10532 14.807C7.20005 14.9288 7.3457 15 7.5 15C7.6543 15 7.79995 14.9288 7.89468 14.807L7.5 14.5ZM0.5 5.5L0.0712535 5.24275C-0.0349854 5.41982 -0.0214495 5.64398 0.105324 5.80697L0.5 5.5ZM3.5 0.5V0H3.2169L3.07125 0.242752L3.5 0.5ZM11.5 0.5L11.9287 0.242752L11.7831 0H11.5V0.5ZM14.5 5.5L14.8947 5.80697C15.0214 5.64398 15.035 5.41982 14.9287 5.24275L14.5 5.5ZM7.89468 14.193L0.894676 5.19303L0.105324 5.80697L7.10532 14.807L7.89468 14.193ZM0.928746 5.75725L3.92875 0.757248L3.07125 0.242752L0.0712535 5.24275L0.928746 5.75725ZM3.5 1H11.5V0H3.5V1ZM11.0713 0.757248L14.0713 5.75725L14.9287 5.24275L11.9287 0.242752L11.0713 0.757248ZM14.1053 5.19303L7.10532 14.193L7.89468 14.807L14.8947 5.80697L14.1053 5.19303Z"
      fill={color}
    />
  {:else}
    <path
      d="M11.7831 0H3.21691L0.0712554 5.24275C-0.0349835 5.41982 -0.0214476 5.64398 0.105326 5.80697L7.10533 14.807C7.20005 14.9288 7.34571 15 7.5 15C7.6543 15 7.79995 14.9288 7.89468 14.807L14.8947 5.80697C15.0215 5.64398 15.035 5.41982 14.9287 5.24275L11.7831 0Z"
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
@prop export let ariaLabel = 'diamond';
-->
