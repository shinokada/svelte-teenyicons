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
  export let ariaLabel = 'ripple';
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
      d="M1.5 1.5L4.56079 4.81585C6.14464 6.53169 8.85536 6.53169 10.4392 4.81585L13.5 1.5M1.5 13.5L4.56079 10.1841C6.14464 8.46831 8.85536 8.46831 10.4392 10.1841L13.5 13.5"
      stroke={color}
    />
  {:else}
    <path
      fill-rule="evenodd"
      clip-rule="evenodd"
      d="M4.19339 5.15499L1.1326 1.83914L1.8674 1.16086L4.92819 4.47671C6.31406 5.97807 8.68594 5.97807 10.0718 4.47671L13.1326 1.16086L13.8674 1.83914L10.8066 5.15499C9.02478 7.08531 5.97522 7.08531 4.19339 5.15499ZM10.0718 10.5233C8.68594 9.02193 6.31406 9.02193 4.92819 10.5233L1.8674 13.8391L1.1326 13.1609L4.19339 9.84501C5.97522 7.91469 9.02478 7.91469 10.8066 9.84501L13.8674 13.1609L13.1326 13.8391L10.0718 10.5233Z"
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
@prop export let ariaLabel = 'ripple';
-->
