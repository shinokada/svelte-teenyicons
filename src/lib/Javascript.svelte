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
  export let ariaLabel = 'javascript';
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
      d="M12.5 8V7.83333C12.5 7.09695 11.903 6.5 11.1667 6.5H10C9.17157 6.5 8.5 7.17157 8.5 8C8.5 8.82843 9.17157 9.5 10 9.5H11C11.8284 9.5 12.5 10.1716 12.5 11C12.5 11.8284 11.8284 12.5 11 12.5H10C9.17157 12.5 8.5 11.8284 8.5 11M6.5 6V11C6.5 11.8284 5.82843 12.5 5 12.5C4.17157 12.5 3.5 11.8284 3.5 11M0.5 0.5H14.5V14.5H0.5V0.5Z"
      stroke={color}
    />
  {:else}
    <path
      fill-rule="evenodd"
      clip-rule="evenodd"
      d="M15 0H0V15H15V0ZM8 8C8 6.89543 8.89543 6 10 6H11.1667C12.1792 6 13 6.82081 13 7.83333V8H12V7.83333C12 7.3731 11.6269 7 11.1667 7H10C9.44772 7 9 7.44772 9 8C9 8.55228 9.44772 9 10 9H11C12.1046 9 13 9.89543 13 11C13 12.1046 12.1046 13 11 13H10C8.89543 13 8 12.1046 8 11H9C9 11.5523 9.44772 12 10 12H11C11.5523 12 12 11.5523 12 11C12 10.4477 11.5523 10 11 10H10C8.89543 10 8 9.10457 8 8ZM6 6V11C6 11.5523 5.55228 12 5 12C4.44772 12 4 11.5523 4 11H3C3 12.1046 3.89543 13 5 13C6.10457 13 7 12.1046 7 11V6H6Z"
      fill={color}
    />
  {/if}
</svg>

<!--
@component
[Go to docs](https://svelte-teenyicons.vercel.app/)
## Props
@prop export let size: string = ctx.size || '15';
@prop export let role: string = ctx.role || 'img';
@prop export let color: string = ctx.color || 'currentColor';
@prop export let variation: 'solid' | 'outline' = 'outline';
@prop export let ariaLabel = 'javascript';
-->
