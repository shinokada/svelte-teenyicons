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
  export let ariaLabel = 'shield tick';
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
      d="M4 7.5L7 10L11 5M7.5 0.5L0.5 4.5V5.21989C0.5 9.52908 3.35661 13.3162 7.5 14.5C11.6434 13.3162 14.5 9.52908 14.5 5.21989V4.5L7.5 0.5Z"
      stroke={color}
      stroke-linejoin="round"
    />
  {:else}
    <path
      fill-rule="evenodd"
      clip-rule="evenodd"
      d="M7.25193 0.0658784C7.40565 -0.0219595 7.59435 -0.0219595 7.74807 0.0658784L14.7481 4.06588C14.9039 4.1549 15 4.32057 15 4.5V5.21989C15 9.75232 11.9954 13.7356 7.63736 14.9808C7.54758 15.0064 7.45242 15.0064 7.36264 14.9808C3.0046 13.7356 0 9.75232 0 5.21989V4.5C0 4.32057 0.096143 4.1549 0.251931 4.06588L7.25193 0.0658784ZM7.0718 10.7107L11.3905 5.31235L10.6096 4.68765L6.92825 9.28933L4.32012 7.11589L3.67993 7.88411L7.0718 10.7107Z"
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
@prop export let ariaLabel = 'shield tick';
-->
