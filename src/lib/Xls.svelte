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
  export let ariaLabel = 'xls';
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
      d="M13.5 3.5H14V3.29289L13.8536 3.14645L13.5 3.5ZM10.5 0.5L10.8536 0.146447L10.7071 0H10.5V0.5ZM6.5 10.5H6V11H6.5V10.5ZM4.5 9.5H5V9.29289L4.85355 9.14645L4.5 9.5ZM2.5 7.5H2V7.70711L2.14645 7.85355L2.5 7.5ZM10.5 6.5V6H10V6.5H10.5ZM10.5 8.5H10V9H10.5V8.5ZM12.5 8.5H13V8H12.5V8.5ZM12.5 10.5V11H13V10.5H12.5ZM2.5 9.5L2.14645 9.14645L2 9.29289V9.5H2.5ZM4.5 7.5L4.85355 7.85355L5 7.70711V7.5H4.5ZM2 5V1.5H1V5H2ZM13 3.5V5H14V3.5H13ZM2.5 1H10.5V0H2.5V1ZM10.1464 0.853553L13.1464 3.85355L13.8536 3.14645L10.8536 0.146447L10.1464 0.853553ZM2 1.5C2 1.22386 2.22386 1 2.5 1V0C1.67157 0 1 0.671573 1 1.5H2ZM1 12V13.5H2V12H1ZM2.5 15H12.5V14H2.5V15ZM14 13.5V12H13V13.5H14ZM12.5 15C13.3284 15 14 14.3284 14 13.5H13C13 13.7761 12.7761 14 12.5 14V15ZM1 13.5C1 14.3284 1.67157 15 2.5 15V14C2.22386 14 2 13.7761 2 13.5H1ZM6 6V10.5H7V6H6ZM6.5 11H9V10H6.5V11ZM4 9.5V11H5V9.5H4ZM4.85355 9.14645L2.85355 7.14645L2.14645 7.85355L4.14645 9.85355L4.85355 9.14645ZM3 7.5V6H2V7.5H3ZM13 6H10.5V7H13V6ZM10 6.5V8.5H11V6.5H10ZM10.5 9H12.5V8H10.5V9ZM12 8.5V10.5H13V8.5H12ZM12.5 10H10V11H12.5V10ZM3 11V9.5H2V11H3ZM2.85355 9.85355L4.85355 7.85355L4.14645 7.14645L2.14645 9.14645L2.85355 9.85355ZM5 7.5V6H4V7.5H5Z"
      fill={color}
    />
  {:else}
    <path
      fill-rule="evenodd"
      clip-rule="evenodd"
      d="M1 1.5C1 0.671573 1.67157 0 2.5 0H10.7071L14 3.29289V13.5C14 14.3284 13.3284 15 12.5 15H2.5C1.67157 15 1 14.3284 1 13.5V1.5ZM3 7.29289V6H2V7.70711L2.79289 8.5L2 9.29289V11H3V9.70711L3.5 9.20711L4 9.70711V11H5V9.29289L4.20711 8.5L5 7.70711V6H4V7.29289L3.5 7.79289L3 7.29289ZM6 6H7V10H9V11H6V6ZM13 6H10V9H12V10H10V11H13V8H11V7H13V6Z"
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
@prop export let ariaLabel = 'xls';
-->
