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
  export let ariaLabel = 'sort alphabetically';
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
      d="M3.5 14.5L3.14645 14.8536C3.24021 14.9473 3.36739 15 3.5 15C3.63261 15 3.75978 14.9473 3.85355 14.8536L3.5 14.5ZM9.5 8.5V8H9V8.5H9.5ZM9.5 14.5H9V15H9.5V14.5ZM3.85355 14.8536L6.85355 11.8536L6.14645 11.1464L3.14645 14.1464L3.85355 14.8536ZM3.85355 14.1464L0.853553 11.1464L0.146447 11.8536L3.14645 14.8536L3.85355 14.1464ZM3 0V14.5H4V0H3ZM9.5 9H12V8H9.5V9ZM12 11H9.5V12H12V11ZM10 11.5V8.5H9V11.5H10ZM13 10C13 10.5523 12.5523 11 12 11V12C13.1046 12 14 11.1046 14 10H13ZM12 9C12.5523 9 13 9.44772 13 10H14C14 8.89543 13.1046 8 12 8V9ZM12 14H9.5V15H12V14ZM10 14.5V11.5H9V14.5H10ZM13 13C13 13.5523 12.5523 14 12 14V15C13.1046 15 14 14.1046 14 13H13ZM12 12C12.5523 12 13 12.4477 13 13H14C14 11.8954 13.1046 11 12 11V12ZM10 7V2.5H9V7H10ZM13 2.5V7H14V2.5H13ZM11.5 1C12.3284 1 13 1.67157 13 2.5H14C14 1.11929 12.8807 0 11.5 0V1ZM10 2.5C10 1.67157 10.6716 1 11.5 1V0C10.1193 0 9 1.11929 9 2.5H10ZM9.5 5H13.5V4H9.5V5Z"
      fill={color}
    />
  {:else}
    <path
      fill-rule="evenodd"
      clip-rule="evenodd"
      d="M3.00001 13.2929V0H4.00001V13.2929L6.14645 11.1464L6.85356 11.8536L3.85356 14.8536C3.75979 14.9473 3.63262 15 3.50001 15C3.3674 15 3.24022 14.9473 3.14645 14.8536L0.146454 11.8536L0.853561 11.1464L3.00001 13.2929ZM11.5 1C10.6716 1 10 1.67157 10 2.5V4H13V2.5C13 1.67157 12.3284 1 11.5 1ZM13 5V7H14V2.5C14 1.11929 12.8807 0 11.5 0C10.1193 0 9.00001 1.11929 9.00001 2.5V7H10V5H13ZM9.00001 8H12C13.1046 8 14 8.89543 14 10C14 10.5973 13.7381 11.1335 13.3229 11.5C13.7381 11.8665 14 12.4027 14 13C14 14.1046 13.1046 15 12 15H9.00001V8ZM12 11C12.5523 11 13 10.5523 13 10C13 9.44772 12.5523 9 12 9H10V11H12ZM10 12H12C12.5523 12 13 12.4477 13 13C13 13.5523 12.5523 14 12 14H10V12Z"
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
@prop export let ariaLabel = 'sort alphabetically';
-->
