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
  export let ariaLabel = 'sort low to high';
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
      d="M11.5 0.5H12C12 0.223858 11.7761 0 11.5 0V0.5ZM4.5 0.5L4.85355 0.146447C4.65829 -0.0488155 4.34171 -0.0488155 4.14645 0.146447L4.5 0.5ZM10 1H11.5V0H10V1ZM11 0.5V6.5H12V0.5H11ZM10 7H13V6H10V7ZM11.578 8H11V9H11.578V8ZM12.9743 11.6581L13.3665 10.4815L12.4179 10.1653L12.0257 11.3419L12.9743 11.6581ZM11 12H12.5V11H11V12ZM11.9743 14.6581L12.9743 11.6581L12.0257 11.3419L11.0257 14.3419L11.9743 14.6581ZM9 10C9 11.1046 9.89543 12 11 12V11C10.4477 11 10 10.5523 10 10H9ZM11 8C9.89543 8 9 8.89543 9 10H10C10 9.44772 10.4477 9 11 9V8ZM11.578 9C12.1823 9 12.609 9.59201 12.4179 10.1653L13.3665 10.4815C13.7735 9.26071 12.8648 8 11.578 8V9ZM4.14645 0.146447L1.14645 3.14645L1.85355 3.85355L4.85355 0.853553L4.14645 0.146447ZM4.14645 0.853553L7.14645 3.85355L7.85355 3.14645L4.85355 0.146447L4.14645 0.853553ZM4 0.5V15H5V0.5H4Z"
      fill={color}
    />
  {:else}
    <path
      fill-rule="evenodd"
      clip-rule="evenodd"
      d="M4.14645 0.146447C4.34172 -0.0488155 4.6583 -0.0488155 4.85356 0.146447L7.85356 3.14645L7.14645 3.85355L5.00001 1.70711V15H4.00001V1.70711L1.85356 3.85355L1.14645 3.14645L4.14645 0.146447ZM11 1H10V7.45058e-09H11.5C11.7761 7.45058e-09 12 0.223858 12 0.5V6H13V7H10V6H11V1ZM9.00001 10C9.00001 8.89543 9.89544 8 11 8H11.578C12.8648 8 13.7735 9.26071 13.3666 10.4815L11.9743 14.6581L11.0257 14.3419L11.8063 12H11C9.89544 12 9.00001 11.1046 9.00001 10ZM12.1396 11L12.4179 10.1653C12.609 9.59201 12.1823 9 11.578 9H11C10.4477 9 10 9.44772 10 10C10 10.5523 10.4477 11 11 11H12.1396Z"
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
@prop export let ariaLabel = 'sort low to high';
-->
