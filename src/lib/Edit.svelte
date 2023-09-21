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
  export let ariaLabel = 'edit';
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
      d="M0.5 10.5L0.146447 10.1464L0 10.2929V10.5H0.5ZM10.5 0.5L10.8536 0.146447C10.6583 -0.0488155 10.3417 -0.0488155 10.1464 0.146447L10.5 0.5ZM14.5 4.5L14.8536 4.85355C15.0488 4.65829 15.0488 4.34171 14.8536 4.14645L14.5 4.5ZM4.5 14.5V15H4.70711L4.85355 14.8536L4.5 14.5ZM0.5 14.5H0C0 14.7761 0.223858 15 0.5 15L0.5 14.5ZM0.853553 10.8536L10.8536 0.853553L10.1464 0.146447L0.146447 10.1464L0.853553 10.8536ZM10.1464 0.853553L14.1464 4.85355L14.8536 4.14645L10.8536 0.146447L10.1464 0.853553ZM14.1464 4.14645L4.14645 14.1464L4.85355 14.8536L14.8536 4.85355L14.1464 4.14645ZM4.5 14H0.5V15H4.5V14ZM1 14.5V10.5H0V14.5H1Z"
      fill={color}
    />
  {:else}
    <path
      d="M10.8536 0.146447C10.6583 -0.0488155 10.3417 -0.0488155 10.1464 0.146447L0 10.2929V14.5C0 14.7761 0.223858 15 0.5 15H4.70711L14.8536 4.85355C15.0488 4.65829 15.0488 4.34171 14.8536 4.14645L10.8536 0.146447Z"
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
@prop export let ariaLabel = 'edit';
-->
