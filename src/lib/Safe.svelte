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
  export let ariaLabel = 'safe';
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
      d="M2.5 3V6M2.5 8V11M2.5 13.5V15M12.5 13.5V15M9.5 9.5C8.39543 9.5 7.5 8.60457 7.5 7.5C7.5 6.39543 8.39543 5.5 9.5 5.5C10.6046 5.5 11.5 6.39543 11.5 7.5C11.5 8.60457 10.6046 9.5 9.5 9.5ZM1.5 0.5H13.5C14.0523 0.5 14.5 0.947715 14.5 1.5V12.5C14.5 13.0523 14.0523 13.5 13.5 13.5H1.5C0.947716 13.5 0.5 13.0523 0.5 12.5V1.5C0.5 0.947715 0.947715 0.5 1.5 0.5Z"
      stroke={color}
    />
  {:else}
    <path
      d="M8 7.5C8 6.67157 8.67157 6 9.5 6C10.3284 6 11 6.67157 11 7.5C11 8.32843 10.3284 9 9.5 9C8.67157 9 8 8.32843 8 7.5Z"
      fill={color}
    />
    <path
      fill-rule="evenodd"
      clip-rule="evenodd"
      d="M1.5 0C0.671573 0 0 0.671573 0 1.5V12.5C0 13.3284 0.671573 14 1.5 14H2V15H3V14H12V15H13V14H13.5C14.3284 14 15 13.3284 15 12.5V1.5C15 0.671573 14.3284 0 13.5 0H1.5ZM2 3V6H3V3H2ZM9.5 5C8.11929 5 7 6.11929 7 7.5C7 8.88071 8.11929 10 9.5 10C10.8807 10 12 8.88071 12 7.5C12 6.11929 10.8807 5 9.5 5ZM2 11V8H3V11H2Z"
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
@prop export let ariaLabel = 'safe';
-->
