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
  export let ariaLabel = 'vector document';
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
      d="M13.5 3.5H14V3.29289L13.8536 3.14645L13.5 3.5ZM10.5 0.5L10.8536 0.146447L10.7071 0H10.5V0.5ZM3.5 4.5V4H3V4.5H3.5ZM5.5 4.5H6V4H5.5V4.5ZM5.5 6.5V7H6V6.5H5.5ZM3.5 6.5H3V7H3.5V6.5ZM11.5 4.5H12V4H11.5V4.5ZM11.5 6.5V7H12V6.5H11.5ZM9.5 6.5H9V7H9.5V6.5ZM9.5 4.5V4H9V4.5H9.5ZM3.5 10.5V10H3V10.5H3.5ZM5.5 10.5H6V10H5.5V10.5ZM5.5 12.5V13H6V12.5H5.5ZM3.5 12.5H3V13H3.5V12.5ZM9.5 10.5V10H9V10.5H9.5ZM9.5 12.5H9V13H9.5V12.5ZM11.5 12.5V13H12V12.5H11.5ZM11.5 10.5H12V10H11.5V10.5ZM12.5 14H2.5V15H12.5V14ZM2 13.5V1.5H1V13.5H2ZM13 3.5V13.5H14V3.5H13ZM2.5 1H10.5V0H2.5V1ZM10.1464 0.853553L13.1464 3.85355L13.8536 3.14645L10.8536 0.146447L10.1464 0.853553ZM2.5 14C2.22386 14 2 13.7761 2 13.5H1C1 14.3284 1.67157 15 2.5 15V14ZM12.5 15C13.3284 15 14 14.3284 14 13.5H13C13 13.7761 12.7761 14 12.5 14V15ZM2 1.5C2 1.22386 2.22386 1 2.5 1V0C1.67157 0 1 0.671574 1 1.5H2ZM3.5 5H5.5V4H3.5V5ZM5 4.5V6.5H6V4.5H5ZM5.5 6H3.5V7H5.5V6ZM4 6.5V4.5H3V6.5H4ZM11 4.5V6.5H12V4.5H11ZM11.5 6H9.5V7H11.5V6ZM10 6.5V4.5H9V6.5H10ZM9.5 5H11.5V4H9.5V5ZM3.5 11H5.5V10H3.5V11ZM5 10.5V12.5H6V10.5H5ZM5.5 12H3.5V13H5.5V12ZM4 12.5V10.5H3V12.5H4ZM9 10.5V12.5H10V10.5H9ZM9.5 13H11.5V12H9.5V13ZM12 12.5V10.5H11V12.5H12ZM11.5 10H9.5V11H11.5V10ZM5.5 6H9.5V5H5.5V6ZM4 6.5V10.5H5V6.5H4ZM10 6.5V10.5H11V6.5H10ZM5.5 12H9.5V11H5.5V12Z"
      fill={color}
    />
  {:else}
    <path d="M9 10V11H6V10H5V7H6V6H9V7H10V10H9Z" fill={color} />
    <path d="M4 5V6H5V5H4Z" fill={color} /> <path d="M10 5V6H11V5H10Z" fill={color} />
    <path d="M4 12V11H5V12H4Z" fill={color} /> <path d="M10 11V12H11V11H10Z" fill={color} />
    <path
      fill-rule="evenodd"
      clip-rule="evenodd"
      d="M1 1.5C1 0.671573 1.67157 0 2.5 0H10.7071L14 3.29289V13.5C14 14.3284 13.3284 15 12.5 15H2.5C1.67157 15 1 14.3284 1 13.5V1.5ZM3 4H6V5H9V4H12V7H11V10H12V13H9V12H6V13H3V10H4V7H3V4Z"
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
@prop export let ariaLabel = 'vector document';
-->
