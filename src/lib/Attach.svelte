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
  export let ariaLabel = 'attach';
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
      d="M13.5 7.5L7.74264 13.2574C6.94699 14.053 5.86786 14.5 4.74264 14.5C2.3995 14.5 0.5 12.6005 0.5 10.2574C0.5 9.13214 0.946991 8.05301 1.74264 7.25736L7.67157 1.32843C8.20201 0.797993 8.92143 0.5 9.67157 0.5C11.2337 0.5 12.5 1.76633 12.5 3.32843C12.5 4.07857 12.202 4.79799 11.6716 5.32843L5.91421 11.0858C5.649 11.351 5.28929 11.5 4.91421 11.5C4.13316 11.5 3.5 10.8668 3.5 10.0858C3.5 9.71071 3.649 9.351 3.91421 9.08579L9.5 3.5"
      stroke={color}
    />
  {:else}
    <path
      fill-rule="evenodd"
      clip-rule="evenodd"
      d="M7.31802 0.974872C7.94222 0.350671 8.78882 0 9.67157 0C11.5098 0 13 1.49019 13 3.32843C13 4.21118 12.6493 5.05778 12.0251 5.68198L6.26777 11.4393C5.90878 11.7983 5.42189 12 4.91421 12C3.85702 12 3 11.143 3 10.0858C3 9.5781 3.20168 9.09122 3.56066 8.73223L9.14645 3.14645L9.85355 3.85355L4.26777 9.43934C4.09632 9.61079 4 9.84332 4 10.0858C4 10.5907 4.40931 11 4.91421 11C5.15668 11 5.38921 10.9037 5.56066 10.7322L11.318 4.97487C11.7547 4.53821 12 3.94596 12 3.32843C12 2.04247 10.9575 1 9.67157 1C9.05404 1 8.46179 1.24531 8.02513 1.68198L2.09619 7.61091C1.39431 8.31279 1 9.26475 1 10.2574C1 12.3244 2.67564 14 4.74264 14C5.73525 14 6.6872 13.6057 7.38909 12.9038L13.1464 7.14645L13.8536 7.85355L8.09619 13.6109C7.20678 14.5003 6.00047 15 4.74264 15C2.12335 15 0 12.8766 0 10.2574C0 8.99953 0.49967 7.79322 1.38909 6.90381L7.31802 0.974872Z"
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
@prop export let ariaLabel = 'attach';
-->
