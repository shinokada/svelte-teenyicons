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
  export let ariaLabel = 'subscript';
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
      d="M12.5 14.5L12.1464 14.1464C12.0034 14.2894 11.9607 14.5045 12.0381 14.6913C12.1155 14.8782 12.2978 15 12.5 15V14.5ZM15 14H12.5V15H15V14ZM12.8536 14.8536L14.6464 13.0607L13.9393 12.3536L12.1464 14.1464L12.8536 14.8536ZM13.7929 11H13.5V12H13.7929V11ZM13.5 11C12.6716 11 12 11.6716 12 12.5H13C13 12.2239 13.2239 12 13.5 12V11ZM15 12.2071C15 11.5404 14.4596 11 13.7929 11V12C13.9073 12 14 12.0927 14 12.2071H15ZM14.6464 13.0607C14.8728 12.8343 15 12.5273 15 12.2071H14C14 12.262 13.9782 12.3147 13.9393 12.3536L14.6464 13.0607ZM1.9 13.8L10.9 1.8L10.1 1.2L1.1 13.2L1.9 13.8ZM1.1 1.8L10.1 13.8L10.9 13.2L1.9 1.2L1.1 1.8Z"
      fill={color}
    />
  {:else}
    <path
      fill-rule="evenodd"
      clip-rule="evenodd"
      d="M6.00001 8.33333L1.90001 13.8L1.10001 13.2L5.37501 7.5L1.10001 1.8L1.90001 1.2L6.00001 6.66667L10.1 1.2L10.9 1.8L6.62501 7.5L10.9 13.2L10.1 13.8L6.00001 8.33333ZM12 12.5C12 11.6716 12.6716 11 13.5 11H13.7929C14.4596 11 15 11.5404 15 12.2071C15 12.5273 14.8728 12.8343 14.6465 13.0607L13.7071 14H15V15H12.5C12.2978 15 12.1155 14.8782 12.0381 14.6913C11.9607 14.5045 12.0035 14.2894 12.1465 14.1464L13.9393 12.3536C13.9782 12.3147 14 12.262 14 12.2071C14 12.0927 13.9073 12 13.7929 12H13.5C13.2239 12 13 12.2239 13 12.5H12Z"
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
@prop export let ariaLabel = 'subscript';
-->
