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
  export let ariaLabel = 'page break';
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
      d="M0.5 8.99347H0V9.99347H0.5V8.99347ZM2.5 9.99347H3V8.99347H2.5V9.99347ZM4.5 8.99347H4V9.99347H4.5V8.99347ZM6.5 9.99347H7V8.99347H6.5V9.99347ZM8.5 8.99347H8V9.99347H8.5V8.99347ZM10.5 9.99347H11V8.99347H10.5V9.99347ZM12.5 8.99347H12V9.99347H12.5V8.99347ZM14.5 9.99347H15V8.99347H14.5V9.99347ZM10.5 0.5L10.8536 0.146447L10.7071 0H10.5V0.5ZM13.5 3.5H14V3.29289L13.8536 3.14645L13.5 3.5ZM0.5 9.99347H2.5V8.99347H0.5V9.99347ZM4.5 9.99347H6.5V8.99347H4.5V9.99347ZM8.5 9.99347H10.5V8.99347H8.5V9.99347ZM12.5 9.99347H14.5V8.99347H12.5V9.99347ZM12.5 14H2.5V15H12.5V14ZM2.5 1H10.5V0H2.5V1ZM10.1464 0.853553L13.1464 3.85355L13.8536 3.14645L10.8536 0.146447L10.1464 0.853553ZM13 3.5V8H14V3.5H13ZM13 11.75V13.5H14V11.75H13ZM2 8V1.5H1V8H2ZM2 13.5V11H1V13.5H2ZM2.5 14C2.22386 14 2 13.7761 2 13.5H1C1 14.3284 1.67157 15 2.5 15V14ZM12.5 15C13.3284 15 14 14.3284 14 13.5H13C13 13.7761 12.7761 14 12.5 14V15ZM2.5 0C1.67157 0 1 0.671573 1 1.5H2C2 1.22386 2.22386 1 2.5 1V0Z"
      fill={color}
    />
  {:else}
    <path d="M1 1.5C1 0.671573 1.67157 0 2.5 0H10.7071L14 3.29289V8H1V1.5Z" fill={color} />
    <path
      d="M1 11H14V13.5C14 14.3284 13.3284 15 12.5 15H2.5C1.67157 15 1 14.3284 1 13.5V11Z"
      fill={color}
    /> <path d="M0 8.99347H3V9.99347H0V8.99347Z" fill={color} />
    <path d="M4 8.99347H7V9.99347H4V8.99347Z" fill={color} />
    <path d="M11 8.99347H8V9.99347H11V8.99347Z" fill={color} />
    <path d="M12 8.99347H15V9.99347H12V8.99347Z" fill={color} />
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
@prop export let ariaLabel = 'page break';
-->
