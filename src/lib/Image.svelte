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
  export let ariaLabel = 'image';
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
      d="M4.5 3.5L4.85355 3.14645C4.65829 2.95118 4.34171 2.95118 4.14645 3.14645L4.5 3.5ZM1.5 1H13.5V0H1.5V1ZM14 1.5V13.5H15V1.5H14ZM13.5 14H1.5V15H13.5V14ZM1 13.5V1.5H0V13.5H1ZM1.5 14C1.22386 14 1 13.7761 1 13.5H0C0 14.3284 0.671573 15 1.5 15V14ZM14 13.5C14 13.7761 13.7761 14 13.5 14V15C14.3284 15 15 14.3284 15 13.5H14ZM13.5 1C13.7761 1 14 1.22386 14 1.5H15C15 0.671573 14.3284 0 13.5 0V1ZM1.5 0C0.671573 0 0 0.671574 0 1.5H1C1 1.22386 1.22386 1 1.5 1V0ZM0.5 11H14.5V10H0.5V11ZM0.853553 7.85355L4.85355 3.85355L4.14645 3.14645L0.146447 7.14645L0.853553 7.85355ZM4.14645 3.85355L11.1464 10.8536L11.8536 10.1464L4.85355 3.14645L4.14645 3.85355ZM10.5 5C10.2239 5 10 4.77614 10 4.5H9C9 5.32843 9.67157 6 10.5 6V5ZM11 4.5C11 4.77614 10.7761 5 10.5 5V6C11.3284 6 12 5.32843 12 4.5H11ZM10.5 4C10.7761 4 11 4.22386 11 4.5H12C12 3.67157 11.3284 3 10.5 3V4ZM10.5 3C9.67157 3 9 3.67157 9 4.5H10C10 4.22386 10.2239 4 10.5 4V3Z"
      fill={color}
    />
  {:else}
    <path
      d="M10.5 3C9.67157 3 9 3.67157 9 4.5C9 5.32843 9.67157 6 10.5 6C11.3284 6 12 5.32843 12 4.5C12 3.67157 11.3284 3 10.5 3Z"
      fill={color}
    />
    <path
      fill-rule="evenodd"
      clip-rule="evenodd"
      d="M0 1.5C0 0.671573 0.671573 0 1.5 0H13.5C14.3284 0 15 0.671573 15 1.5V13.5C15 13.6035 14.9895 13.7047 14.9695 13.8023C14.9399 13.9468 14.8896 14.0838 14.8217 14.2099C14.5685 14.6803 14.0716 15 13.5 15H1.5C0.671573 15 0 14.3284 0 13.5V1.5ZM4.84923 3.14214L4.5 2.79291L1 6.29291V1.5C1 1.22386 1.22386 1 1.5 1H13.5C13.7761 1 14 1.22386 14 1.5V10H11.7071L4.85359 3.14645C4.85215 3.145 4.85069 3.14357 4.84923 3.14214Z"
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
@prop export let ariaLabel = 'image';
-->
