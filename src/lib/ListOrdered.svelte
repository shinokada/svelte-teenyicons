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
  export let ariaLabel = 'list ordered';
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
      d="M0.5 13.5L0.146447 13.1464C0.00344761 13.2894 -0.0393303 13.5045 0.0380602 13.6913C0.115451 13.8782 0.297769 14 0.5 14V13.5ZM1.5 2.5H2V2H1.5V2.5ZM5 8H15V7H5V8ZM5 4H15V3H5V4ZM5 12H15V11H5V12ZM3 13H0.5V14H3V13ZM0.853553 13.8536L2.64645 12.0607L1.93934 11.3536L0.146447 13.1464L0.853553 13.8536ZM1.79289 10H1.5V11H1.79289V10ZM1.5 10C0.671573 10 0 10.6716 0 11.5H1C1 11.2239 1.22386 11 1.5 11V10ZM3 11.2071C3 10.5404 2.45956 10 1.79289 10V11C1.90728 11 2 11.0927 2 11.2071H3ZM2.64645 12.0607C2.87282 11.8343 3 11.5273 3 11.2071H2C2 11.262 1.97818 11.3147 1.93934 11.3536L2.64645 12.0607ZM0 6H3V5H0V6ZM2 5.5V2.5H1V5.5H2ZM1.5 2H0V3H1.5V2Z"
      fill={color}
    />
  {:else}
    <path
      fill-rule="evenodd"
      clip-rule="evenodd"
      d="M7.24358e-08 2H2V5H3V6H7.24358e-08V5H1V3H7.24358e-08V2ZM15 4H5V3H15V4ZM15 8H5V7H15V8ZM7.24358e-08 11.5C7.24358e-08 10.6716 0.671573 10 1.5 10H1.79289C2.45956 10 3 10.5404 3 11.2071C3 11.5273 2.87282 11.8343 2.64645 12.0607L1.70711 13H3V14H0.5C0.297769 14 0.115451 13.8782 0.0380603 13.6913C-0.0393302 13.5045 0.00344768 13.2894 0.146447 13.1464L1.93934 11.3536C1.97818 11.3147 2 11.262 2 11.2071C2 11.0927 1.90728 11 1.79289 11H1.5C1.22386 11 1 11.2239 1 11.5H7.24358e-08ZM15 12H5V11H15V12Z"
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
@prop export let ariaLabel = 'list ordered';
-->
