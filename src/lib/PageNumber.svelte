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
  export let ariaLabel = 'page number';
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
      d="M10.5 0.5L10.8536 0.146447L10.7071 0H10.5V0.5ZM13.5 3.5H14V3.29289L13.8536 3.14645L13.5 3.5ZM9.5 12.5L9.14645 12.1464C9.00345 12.2894 8.96067 12.5045 9.03806 12.6913C9.11545 12.8782 9.29777 13 9.5 13V12.5ZM12.5 14H2.5V15H12.5V14ZM2.5 1H10.5V0H2.5V1ZM10.1464 0.853553L13.1464 3.85355L13.8536 3.14645L10.8536 0.146447L10.1464 0.853553ZM2.5 14C2.22386 14 2 13.7761 2 13.5H1C1 14.3284 1.67157 15 2.5 15V14ZM12.5 15C13.3284 15 14 14.3284 14 13.5H13C13 13.7761 12.7761 14 12.5 14V15ZM2.5 0C1.67157 0 1 0.671573 1 1.5H2C2 1.22386 2.22386 1 2.5 1V0ZM12 12H9.5V13H12V12ZM9.85355 12.8536L11.6464 11.0607L10.9393 10.3536L9.14645 12.1464L9.85355 12.8536ZM10.7929 9H10.5V10H10.7929V9ZM10.5 9C9.67157 9 9 9.67157 9 10.5H10C10 10.2239 10.2239 10 10.5 10V9ZM12 10.2071C12 9.54044 11.4596 9 10.7929 9V10C10.9073 10 11 10.0927 11 10.2071H12ZM11.6464 11.0607C11.8728 10.8343 12 10.5273 12 10.2071H11C11 10.262 10.9782 10.3147 10.9393 10.3536L11.6464 11.0607ZM13 3.5V13.5H14V3.5H13ZM2 13.5V1.5H1V13.5H2Z"
      fill={color}
    />
  {:else}
    <path
      fill-rule="evenodd"
      clip-rule="evenodd"
      d="M1 1.5C1 0.671573 1.67157 0 2.5 0H10.7071L14 3.29289V13.5C14 14.3284 13.3284 15 12.5 15H2.5C1.67157 15 1 14.3284 1 13.5V1.5ZM10.5 9C9.67159 9 9.00001 9.67157 9.00001 10.5H10C10 10.2239 10.2239 10 10.5 10H10.7929C10.9073 10 11 10.0927 11 10.2071C11 10.262 10.9782 10.3147 10.9394 10.3536L9.14646 12.1464C9.00346 12.2894 8.96068 12.5045 9.03807 12.6913C9.11547 12.8782 9.29778 13 9.50001 13H12V12H10.7071L11.6465 11.0607C11.8728 10.8343 12 10.5273 12 10.2071C12 9.54044 11.4596 9 10.7929 9H10.5Z"
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
@prop export let ariaLabel = 'page number';
-->
