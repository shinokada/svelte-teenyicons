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
  export let ariaLabel = 'ab testing';
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
      d="M1.5 11V6.5C1.5 5.39543 2.39543 4.5 3.5 4.5C4.60457 4.5 5.5 5.39543 5.5 6.5V11M1.5 8.5H5.5M12 7.5H9.5M12 7.5C12.8284 7.5 13.5 6.82843 13.5 6C13.5 5.17157 12.8284 4.5 12 4.5H9.5V7.5M12 7.5C12.8284 7.5 13.5 8.17157 13.5 9C13.5 9.82843 12.8284 10.5 12 10.5H9.5V7.5M7.5 1V14"
      stroke={color}
    />
  {:else}
    <path d="M3.5 5C2.67157 5 2 5.67157 2 6.5V8H5V6.5C5 5.67157 4.32843 5 3.5 5Z" fill={color} />
    <path
      fill-rule="evenodd"
      clip-rule="evenodd"
      d="M0 2.5C0 1.67157 0.671573 1 1.5 1H5.5C6.32843 1 7 1.67157 7 2.5V12.5C7 13.3284 6.32843 14 5.5 14H1.5C0.671573 14 0 13.3284 0 12.5V2.5ZM2 11V9H5V11H6V6.5C6 5.11929 4.88071 4 3.5 4C2.11929 4 1 5.11929 1 6.5V11H2Z"
      fill={color}
    /> <path d="M12 7H10V5H12C12.5523 5 13 5.44772 13 6C13 6.55228 12.5523 7 12 7Z" fill={color} />
    <path d="M12 10H10V8H12C12.5523 8 13 8.44772 13 9C13 9.55228 12.5523 10 12 10Z" fill={color} />
    <path
      fill-rule="evenodd"
      clip-rule="evenodd"
      d="M8 2.5C8 1.67157 8.67157 1 9.5 1H13.5C14.3284 1 15 1.67157 15 2.5V12.5C15 13.3284 14.3284 14 13.5 14H9.5C8.67157 14 8 13.3284 8 12.5V2.5ZM12 4H9V11H12C13.1046 11 14 10.1046 14 9C14 8.40265 13.7381 7.86647 13.3229 7.5C13.7381 7.13353 14 6.59735 14 6C14 4.89543 13.1046 4 12 4Z"
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
@prop export let ariaLabel = 'ab testing';
-->
