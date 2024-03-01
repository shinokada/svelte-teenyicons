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
  export let ariaLabel = 'c sharp';
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
      d="M9.5 5V10M11.5 5V10M8 6.5H13M8 8.5H13M8 10L7.59787 10.2011C7.20469 10.3977 6.77114 10.5 6.33156 10.5C4.76773 10.5 3.5 9.23227 3.5 7.66844V7.33156C3.5 5.76773 4.76773 4.5 6.33156 4.5C6.77114 4.5 7.20469 4.60235 7.59787 4.79894L8 5M1.5 10.5V4.5L7.5 1L13.5 4.5V10.5L7.5 14L1.5 10.5Z"
      stroke={color}
    />
  {:else}
    <path d="M10 8V7H11V8H10Z" fill={color} />
    <path
      fill-rule="evenodd"
      clip-rule="evenodd"
      d="M7.5 0.421143L14 4.21281V10.7872L7.5 14.5788L1 10.7872V4.21281L7.5 0.421143ZM6.33156 4C4.49159 4 3 5.49159 3 7.33156V7.66844C3 9.50841 4.49159 11 6.33156 11C6.84877 11 7.35887 10.8796 7.82148 10.6483L8.22361 10.4472L7.77639 9.55279L7.37426 9.75385C7.05052 9.91573 6.69352 10 6.33156 10C5.04387 10 4 8.95613 4 7.66844V7.33156C4 6.04387 5.04387 5 6.33156 5C6.69352 5 7.05052 5.08427 7.37426 5.24615L7.77639 5.44721L8.22361 4.55279L7.82148 4.35172C7.35887 4.12042 6.84877 4 6.33156 4ZM9 5V6H8V7H9V8H8V9H9V10H10V9H11V10H12V9H13V8H12V7H13V6H12V5H11V6H10V5H9Z"
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
@prop export let ariaLabel = 'c sharp';
-->
