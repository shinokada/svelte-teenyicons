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
  export let ariaLabel = 'wand';
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
      d="M6.85344 8.84842L7.20711 8.49498L6.50023 7.78764L6.14656 8.14108L6.85344 8.84842ZM9 10.4935V10.9935H10V10.4935H9ZM10 9.49414V8.99414H9V9.49414H10ZM9 1.49939V1.99939H10V1.49939H9ZM10 0.5V0H9V0.5H10ZM4.5 4.99683H4V5.99683H4.5V4.99683ZM5.5 5.99683H6V4.99683H5.5V5.99683ZM13.5 4.99683H13V5.99683H13.5V4.99683ZM14.5 5.99683H15V4.99683H14.5V5.99683ZM12.1466 2.14512L11.7929 2.49856L12.4998 3.20589L12.8534 2.85244L12.1466 2.14512ZM13.8534 1.85305L14.2071 1.49961L13.5002 0.792283L13.1466 1.14573L13.8534 1.85305ZM5.85345 1.14573L5.49978 0.792283L4.79289 1.49961L5.14655 1.85305L5.85345 1.14573ZM6.14655 2.85244L6.50022 3.20589L7.20711 2.49856L6.85345 2.14512L6.14655 2.85244ZM12.8534 8.14109L12.4998 7.78764L11.7929 8.49497L12.1466 8.84841L12.8534 8.14109ZM13.1466 9.8478L13.5002 10.2012L14.2071 9.49393L13.8534 9.14048L13.1466 9.8478ZM0.853438 14.8445L6.85344 8.84842L6.14656 8.14108L0.146562 14.1372L0.853438 14.8445ZM10 10.4935V9.49414H9V10.4935H10ZM10 1.49939V0.5H9V1.49939H10ZM4.5 5.99683H5.5V4.99683H4.5V5.99683ZM13.5 5.99683H14.5V4.99683H13.5V5.99683ZM12.8534 2.85244L13.8534 1.85305L13.1466 1.14573L12.1466 2.14512L12.8534 2.85244ZM5.14655 1.85305L6.14655 2.85244L6.85345 2.14512L5.85345 1.14573L5.14655 1.85305ZM12.1466 8.84841L13.1466 9.8478L13.8534 9.14048L12.8534 8.14109L12.1466 8.84841Z"
      fill={color}
    />
  {:else}
    <path
      fill-rule="evenodd"
      clip-rule="evenodd"
      d="M10 0V1.99939H9.00001V0H10ZM5.4998 0.792283L7.20712 2.49856L6.50023 3.20589L4.79291 1.49961L5.4998 0.792283ZM14.2071 1.49961L12.4998 3.20589L11.7929 2.49856L13.5002 0.792283L14.2071 1.49961ZM4.00001 4.99683H6.00001V5.99683H4.00001V4.99683ZM13 4.99683H15V5.99683H13V4.99683ZM7.20712 8.49498L0.853452 14.8445L0.146576 14.1372L6.50024 7.78764L7.20712 8.49498ZM12.4998 7.78764L14.2071 9.49393L13.5002 10.2012L11.7929 8.49497L12.4998 7.78764ZM10 8.99414V10.9935H9.00001V8.99414H10Z"
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
@prop export let ariaLabel = 'wand';
-->
