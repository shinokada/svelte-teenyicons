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
  export let ariaLabel = 'messenger';
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
      d="M2.93478 12.2643L3.41722 12.3956C3.46886 12.206 3.40458 12.0036 3.25296 11.8786L2.93478 12.2643ZM2.32609 14.5L1.84365 14.3687C1.79246 14.5567 1.85516 14.7573 2.00431 14.8827C2.15345 15.0081 2.36187 15.0354 2.5383 14.9527L2.32609 14.5ZM4.76087 13.3587L4.9491 12.8955C4.81999 12.843 4.67484 12.8468 4.54865 12.906L4.76087 13.3587ZM6.5 6.5L6.8 6.1L6.5072 5.8804L6.20938 6.09313L6.5 6.5ZM8.5 8L8.2 8.4L8.51633 8.63725L8.82009 8.38411L8.5 8ZM7.5 0C3.37858 0 0 3.20099 0 7.19565H1C1 3.79466 3.88855 1 7.5 1V0ZM0 7.19565C0 9.38419 1.02256 11.335 2.6166 12.65L3.25296 11.8786C1.87049 10.7381 1 9.06224 1 7.19565H0ZM2.45234 12.1329L1.84365 14.3687L2.80853 14.6313L3.41722 12.3956L2.45234 12.1329ZM2.5383 14.9527L4.97309 13.8114L4.54865 12.906L2.11387 14.0473L2.5383 14.9527ZM4.57264 13.8219C5.47308 14.1878 6.46213 14.3913 7.5 14.3913V13.3913C6.59369 13.3913 5.73232 13.2137 4.9491 12.8955L4.57264 13.8219ZM7.5 14.3913C11.6214 14.3913 15 11.1903 15 7.19565H14C14 10.5966 11.1114 13.3913 7.5 13.3913V14.3913ZM15 7.19565C15 3.20099 11.6214 0 7.5 0V1C11.1114 1 14 3.79466 14 7.19565H15ZM3.29062 9.40687L6.79062 6.90687L6.20938 6.09313L2.70938 8.59313L3.29062 9.40687ZM6.2 6.9L8.2 8.4L8.8 7.6L6.8 6.1L6.2 6.9ZM8.82009 8.38411L11.8201 5.88411L11.1799 5.11589L8.17991 7.61589L8.82009 8.38411Z"
      fill={color}
    />
  {:else}
    <path
      fill-rule="evenodd"
      clip-rule="evenodd"
      d="M0 7.19565C0 3.20099 3.37858 0 7.5 0C11.6214 0 15 3.20099 15 7.19565C15 11.1903 11.6214 14.3913 7.5 14.3913C6.54087 14.3913 5.62342 14.2175 4.77908 13.9024L2.5383 14.9527C2.36187 15.0354 2.15345 15.0081 2.00431 14.8827C1.85516 14.7573 1.79246 14.5567 1.84365 14.3687L2.36957 12.437C0.917685 11.1288 0 9.26893 0 7.19565ZM8.51642 8.63725L11.8202 5.88411L11.18 5.11589L8.48376 7.36275L6.5073 5.8804L2.70947 8.59313L3.29071 9.40687L6.49289 7.1196L8.51642 8.63725Z"
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
@prop export let ariaLabel = 'messenger';
-->
