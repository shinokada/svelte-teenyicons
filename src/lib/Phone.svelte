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
  export let ariaLabel = 'phone';
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
      d="M4.71922 0.5H2.5C1.39543 0.5 0.5 1.39543 0.5 2.5V4.5C0.5 10.0228 4.97715 14.5 10.5 14.5H12.5C13.6046 14.5 14.5 13.6046 14.5 12.5V11.118C14.5 10.7393 14.286 10.393 13.9472 10.2236L11.5313 9.01564C10.987 8.74349 10.3278 9.01652 10.1354 9.59384L9.83762 10.4871C9.64474 11.0658 9.05118 11.4102 8.45309 11.2906C6.05929 10.8119 4.18814 8.94071 3.70938 6.54691C3.58976 5.94882 3.93422 5.35526 4.51286 5.16238L5.62149 4.79284C6.11721 4.6276 6.40214 4.10855 6.2754 3.60162L5.68937 1.25746C5.57807 0.812297 5.17809 0.5 4.71922 0.5Z"
      stroke={color}
    />
  {:else}
    <path
      d="M2.5 0C1.11929 0 0 1.11929 0 2.5V4.5C0 10.299 4.70101 15 10.5 15H12.5C13.8807 15 15 13.8807 15 12.5V11.118C15 10.5499 14.679 10.0305 14.1708 9.77639L11.7549 8.56843C10.9384 8.1602 9.94971 8.56975 9.66105 9.43573L9.36328 10.329C9.25014 10.6684 8.90197 10.8705 8.55114 10.8003C6.35528 10.3612 4.63885 8.64472 4.19967 6.44886C4.12951 6.09803 4.33156 5.74986 4.67097 5.63672L5.7796 5.26718C6.52319 5.01932 6.95058 4.24075 6.76048 3.48035L6.17444 1.1362C6.0075 0.468446 5.40752 0 4.71922 0H2.5Z"
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
@prop export let ariaLabel = 'phone';
-->
