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
  export let ariaLabel = 'phonecall blocked';
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
      d="M13.5 1.5L9.5 5.5M2.5 0.5H4.71922C5.17809 0.5 5.57807 0.812297 5.68937 1.25746L6.2754 3.60162C6.40214 4.10855 6.11721 4.6276 5.62149 4.79284L4.51286 5.16238C3.93422 5.35526 3.58976 5.94882 3.70938 6.54691C4.18814 8.94071 6.05929 10.8119 8.45309 11.2906C9.05118 11.4102 9.64474 11.0658 9.83762 10.4871L10.1354 9.59384C10.3278 9.01652 10.987 8.74349 11.5313 9.01564L13.9472 10.2236C14.286 10.393 14.5 10.7393 14.5 11.118V12.5C14.5 13.6046 13.6046 14.5 12.5 14.5H10.5C4.97715 14.5 0.5 10.0228 0.5 4.5V2.5C0.5 1.39543 1.39543 0.5 2.5 0.5ZM11.5 6.5C9.84315 6.5 8.5 5.15685 8.5 3.5C8.5 1.84315 9.84315 0.5 11.5 0.5C13.1569 0.5 14.5 1.84315 14.5 3.5C14.5 5.15685 13.1569 6.5 11.5 6.5Z"
      stroke={color}
    />
  {:else}
    <path
      d="M0 2.5C0 1.11929 1.11929 0 2.5 0H4.71922C5.40752 0 6.0075 0.468446 6.17444 1.1362L6.76048 3.48035C6.95058 4.24075 6.52319 5.01932 5.7796 5.26718L4.67097 5.63672C4.33156 5.74986 4.12951 6.09803 4.19967 6.44886C4.63885 8.64472 6.35528 10.3612 8.55114 10.8003C8.90197 10.8705 9.25014 10.6684 9.36328 10.329L9.66105 9.43573C9.94971 8.56975 10.9384 8.1602 11.7549 8.56843L14.1708 9.77639C14.679 10.0305 15 10.5499 15 11.118V12.5C15 13.8807 13.8807 15 12.5 15H10.5C4.70101 15 0 10.299 0 4.5V2.5Z"
      fill={color}
    />
    <path
      fill-rule="evenodd"
      clip-rule="evenodd"
      d="M8 3.5C8 1.567 9.567 0 11.5 0C13.433 0 15 1.567 15 3.5C15 5.433 13.433 7 11.5 7C9.567 7 8 5.433 8 3.5ZM11.5 1C10.1193 1 9 2.11929 9 3.5C9 4.00955 9.15244 4.4835 9.41422 4.87872L12.8787 1.41422C12.4835 1.15245 12.0096 1 11.5 1ZM11.5 6C10.9905 6 10.5165 5.84757 10.1213 5.58582L13.5858 2.12133C13.8476 2.51654 14 2.99047 14 3.5C14 4.88071 12.8807 6 11.5 6Z"
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
@prop export let ariaLabel = 'phonecall blocked';
-->
