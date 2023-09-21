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
  export let ariaLabel = 'history';
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
      d="M2.5 12.399L2.87012 12.0628L2.86375 12.0558L2.85712 12.049L2.5 12.399ZM3.5 13.5V14H4V13.5H3.5ZM7 14.4824L7.01757 13.9827L6.9648 14.9812L7 14.4824ZM7.5 7.5H7C7 7.63261 7.05268 7.75979 7.14645 7.85355L7.5 7.5ZM14 7.5C14 11.0899 11.0899 14 7.5 14V15C11.6421 15 15 11.6421 15 7.5H14ZM7.5 1C11.0899 1 14 3.91015 14 7.5H15C15 3.35786 11.6421 0 7.5 0V1ZM7.5 0C3.35786 0 0 3.35786 0 7.5H1C1 3.91015 3.91015 1 7.5 1V0ZM2.85712 12.049C1.7078 10.8762 1 9.27124 1 7.5H0C0 9.54337 0.817823 11.3967 2.14288 12.7489L2.85712 12.049ZM2.12988 12.7351L3.12988 13.8362L3.87012 13.1638L2.87012 12.0628L2.12988 12.7351ZM7.5 14C7.34364 14 7.18865 13.9945 7.0352 13.9837L6.9648 14.9812C7.14166 14.9937 7.32013 15 7.5 15V14ZM7.51757 14.0003L7.01757 13.9827L6.98243 14.9821L7.48243 14.9997L7.51757 14.0003ZM7 3V7.5H8V3H7ZM7.14645 7.85355L10.1464 10.8536L10.8536 10.1464L7.85355 7.14645L7.14645 7.85355ZM0 14H3.5V13H0V14ZM4 13.5V10H3V13.5H4Z"
      fill={color}
    />
  {:else}
    <path
      fill-rule="evenodd"
      clip-rule="evenodd"
      d="M0 7.5C0 3.35786 3.35786 0 7.5 0C11.6421 0 15 3.35786 15 7.5C15 11.6421 11.6421 15 7.5 15C7.32013 15 7.14166 14.9937 6.9648 14.9812L7.01757 13.9827L7.50862 14C11.0945 13.9953 14 11.087 14 7.5C14 3.91015 11.0899 1 7.5 1C3.91015 1 1 3.91015 1 7.5C1 9.27124 1.7078 10.8762 2.85712 12.049L2.86375 12.0558L3 12.2058V10H4V14H0V13H2.37043L2.13613 12.742C0.815047 11.3904 0 9.5399 0 7.5ZM7 7.5V3H8V7.29289L10.8536 10.1464L10.1464 10.8536L7.14645 7.85355C7.05268 7.75979 7 7.63261 7 7.5Z"
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
@prop export let ariaLabel = 'history';
-->
