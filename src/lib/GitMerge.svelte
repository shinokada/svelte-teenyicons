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
  export let ariaLabel = 'git merge';
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
      d="M2.5 10.5C1.39543 10.5 0.5 11.3954 0.5 12.5C0.5 13.6046 1.39543 14.5 2.5 14.5C3.60457 14.5 4.5 13.6046 4.5 12.5C4.5 11.3954 3.60457 10.5 2.5 10.5ZM2.5 10.5V4.5M4.5 2.5C4.5 1.39543 3.60457 0.5 2.5 0.5C1.39543 0.5 0.5 1.39543 0.5 2.5C0.5 3.60457 1.39543 4.5 2.5 4.5M4.5 2.5C4.5 3.60457 3.60457 4.5 2.5 4.5M4.5 2.5H9.5C11.1569 2.5 12.5 3.84315 12.5 5.5V7.5M12.5 7.5C11.3954 7.5 10.5 8.39543 10.5 9.5C10.5 10.6046 11.3954 11.5 12.5 11.5C13.6046 11.5 14.5 10.6046 14.5 9.5C14.5 8.39543 13.6046 7.5 12.5 7.5Z"
      stroke={color}
    />
  {:else}
    <path
      d="M2.5 0C1.11929 0 0 1.11929 0 2.5C0 3.70948 0.85888 4.71836 2 4.94999V10.05C0.85888 10.2816 0 11.2905 0 12.5C0 13.8807 1.11929 15 2.5 15C3.88071 15 5 13.8807 5 12.5C5 11.2905 4.14112 10.2816 3 10.05V4.94999C3.97957 4.75115 4.75115 3.97956 4.94999 3H9.5C10.8807 3 12 4.11929 12 5.5V7.05001C10.8589 7.28164 10 8.29052 10 9.5C10 10.8807 11.1193 12 12.5 12C13.8807 12 15 10.8807 15 9.5C15 8.29052 14.1411 7.28164 13 7.05001V5.5C13 3.567 11.433 2 9.5 2H4.94999C4.71836 0.85888 3.70948 0 2.5 0Z"
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
@prop export let ariaLabel = 'git merge';
-->
