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
  export let ariaLabel = 'loop';
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
      d="M14.5 3.5L14.8536 3.85355C15.0488 3.65829 15.0488 3.34171 14.8536 3.14645L14.5 3.5ZM0.5 11.5L0.146447 11.1464C-0.0488153 11.3417 -0.0488153 11.6583 0.146447 11.8536L0.5 11.5ZM11.1464 0.853553L14.1464 3.85355L14.8536 3.14645L11.8536 0.146447L11.1464 0.853553ZM14.1464 3.14645L11.1464 6.14645L11.8536 6.85355L14.8536 3.85355L14.1464 3.14645ZM3.85355 14.1464L0.853554 11.1464L0.146447 11.8536L3.14644 14.8536L3.85355 14.1464ZM0.853554 11.8536L3.85355 8.85355L3.14645 8.14645L0.146447 11.1464L0.853554 11.8536ZM0.5 12H11.5V11H0.5V12ZM15 8.5V7H14V8.5H15ZM11.5 12C13.433 12 15 10.433 15 8.5H14C14 9.88071 12.8807 11 11.5 11V12ZM14.5 3H3.5V4H14.5V3ZM0 6.5V8H1V6.5H0ZM3.5 3C1.567 3 0 4.567 0 6.5H1C1 5.11929 2.11929 4 3.5 4V3Z"
      fill={color}
    />
  {:else}
    <path
      fill-rule="evenodd"
      clip-rule="evenodd"
      d="M13.2929 3.00001L11.1464 0.853561L11.8536 0.146454L14.8536 3.14645C15.0488 3.34172 15.0488 3.6583 14.8536 3.85356L11.8536 6.85356L11.1464 6.14645L13.2929 4.00001H3.5C2.11929 4.00001 1 5.1193 1 6.50001V8.00001H0V6.50001C0 4.56701 1.567 3.00001 3.5 3.00001H13.2929ZM15 7.00001V8.50001C15 10.433 13.433 12 11.5 12H1.70711L3.85355 14.1465L3.14644 14.8536L0.146447 11.8536C-0.0488153 11.6583 -0.0488153 11.3417 0.146447 11.1465L3.14645 8.14645L3.85355 8.85356L1.70711 11H11.5C12.8807 11 14 9.88072 14 8.50001V7.00001H15Z"
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
@prop export let ariaLabel = 'loop';
-->
