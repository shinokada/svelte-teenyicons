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
  export let ariaLabel = 'message minus';
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
      d="M5.5 11.4928L5.91594 11.2154C5.8232 11.0763 5.66712 10.9928 5.5 10.9928V11.4928ZM7.5 14.4909L7.08406 14.7683C7.1768 14.9074 7.33288 14.9909 7.5 14.9909C7.66712 14.9909 7.8232 14.9074 7.91594 14.7683L7.5 14.4909ZM9.5 11.4928V10.9928C9.33288 10.9928 9.1768 11.0763 9.08406 11.2154L9.5 11.4928ZM5.08406 11.7703L7.08406 14.7683L7.91594 14.2134L5.91594 11.2154L5.08406 11.7703ZM7.91594 14.7683L9.91594 11.7703L9.08406 11.2154L7.08406 14.2134L7.91594 14.7683ZM9.5 11.9928H13.5V10.9928H9.5V11.9928ZM13.5 11.9928C14.3288 11.9928 15 11.3226 15 10.4935H14C14 10.7697 13.7772 10.9928 13.5 10.9928V11.9928ZM15 10.4935V1.49935H14V10.4935H15ZM15 1.49935C15 0.670259 14.3288 0 13.5 0V1C13.7772 1 14 1.22316 14 1.49935H15ZM13.5 0H1.5V1H13.5V0ZM1.5 0C0.671165 0 0 0.670259 0 1.49935H1C1 1.22316 1.22283 1 1.5 1V0ZM0 1.49935V10.4935H1V1.49935H0ZM0 10.4935C0 11.3226 0.671165 11.9928 1.5 11.9928V10.9928C1.22284 10.9928 1 10.7697 1 10.4935H0ZM1.5 11.9928H5.5V10.9928H1.5V11.9928ZM5 7H10V6H5V7Z"
      fill={color}
    />
  {:else}
    <path
      fill-rule="evenodd"
      clip-rule="evenodd"
      d="M0 1.49935C0 0.670259 0.671165 0 1.5 0H13.5C14.3288 0 15 0.670259 15 1.49935V10.4935C15 11.3226 14.3288 11.9928 13.5 11.9928H9.7675L7.91594 14.7683C7.8232 14.9074 7.66712 14.9909 7.5 14.9909C7.33288 14.9909 7.1768 14.9074 7.08406 14.7683L5.2325 11.9928H1.5C0.671165 11.9928 0 11.3226 0 10.4935V1.49935ZM5 7H10V6H5V7Z"
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
@prop export let ariaLabel = 'message minus';
-->
