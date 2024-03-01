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
  export let ariaLabel = 'ruby';
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
      d="M14.5 14.5V15H15V14.5H14.5ZM14.5 0.5H15V0H14.5V0.5ZM8.5 0.5V0H8.29289L8.14645 0.146447L8.5 0.5ZM0.5 8.5L0.146447 8.14645L0 8.29289V8.5H0.5ZM0.5 14.5H0V15H0.5V14.5ZM4.5 10.5L4.27639 10.9472L4.29499 10.9565L4.3143 10.9642L4.5 10.5ZM4.5 4.5V4C4.22386 4 4 4.22386 4 4.5H4.5ZM10.5 4.5L10.9642 4.3143L10.9565 4.29499L10.9472 4.27639L10.5 4.5ZM15 14.5V0.5H14V14.5H15ZM14.5 0H8.5V1H14.5V0ZM8.14645 0.146447L0.146447 8.14645L0.853553 8.85355L8.85355 0.853553L8.14645 0.146447ZM0 8.5V14.5H1V8.5H0ZM0.5 15H14.5V14H0.5V15ZM14.1464 0.146447L0.146447 14.1464L0.853553 14.8536L14.8536 0.853553L14.1464 0.146447ZM5 10.5V4.5H4V10.5H5ZM4.5 5H10.5V4H4.5V5ZM4.3143 10.9642L14.3143 14.9642L14.6857 14.0358L4.6857 10.0358L4.3143 10.9642ZM10.0358 4.6857L14.0358 14.6857L14.9642 14.3143L10.9642 4.3143L10.0358 4.6857ZM8.05279 0.723607L10.0528 4.72361L10.9472 4.27639L8.94721 0.276393L8.05279 0.723607ZM0.276393 8.94721L4.27639 10.9472L4.72361 10.0528L0.723607 8.05279L0.276393 8.94721Z"
      fill={color}
    />
  {:else}
    <path d="M4.29301 4L8.05751 0.235504L9.73062 4H4.29301Z" fill={color} />
    <path d="M14.293 0L10.6613 3.63175L9.04716 0H14.293Z" fill={color} />
    <path d="M0.235501 8.05751L4.00012 9.73067V4.29289L0.235501 8.05751Z" fill={color} />
    <path d="M3.63174 10.6613L0.000118256 9.04721V14.2929L3.63174 10.6613Z" fill={color} />
    <path d="M5.00012 9.29289L9.29301 5H5.00012V9.29289Z" fill={color} />
    <path d="M15.0001 13.731L11.093 4.61427L15.0001 0.707107V13.731Z" fill={color} />
    <path d="M14.048 14.048L10.3314 5.37585L5.37584 10.3314L14.048 14.048Z" fill={color} />
    <path d="M4.61427 11.093L13.7307 15H0.707225L4.61427 11.093Z" fill={color} />
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
@prop export let ariaLabel = 'ruby';
-->
