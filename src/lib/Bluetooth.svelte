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
  export let ariaLabel = 'bluetooth';
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
      d="M7.5 14.5H7C7 14.6864 7.10373 14.8574 7.26909 14.9435C7.43446 15.0296 7.634 15.0165 7.78673 14.9096L7.5 14.5ZM7.5 0.5L7.78673 0.090384C7.634 -0.016531 7.43446 -0.0295882 7.26909 0.0565107C7.10373 0.14261 7 0.313562 7 0.5L7.5 0.5ZM12.5 4L12.7817 4.41311C12.9174 4.32059 12.999 4.16732 13 4.00308C13.001 3.83884 12.9213 3.68457 12.7867 3.59038L12.5 4ZM12.5 11L12.7867 11.4096C12.9213 11.3154 13.001 11.1612 13 10.9969C12.999 10.8327 12.9174 10.6794 12.7817 10.5869L12.5 11ZM8 14.5V7.40909H7V14.5H8ZM8 7.40909V0.5H7V7.40909H8ZM7.21327 0.909616L12.2133 4.40962L12.7867 3.59038L7.78673 0.090384L7.21327 0.909616ZM12.2183 3.58689L7.21833 6.99598L7.78167 7.8222L12.7817 4.41311L12.2183 3.58689ZM7.21833 6.99598L1.21833 11.0869L1.78167 11.9131L7.78167 7.8222L7.21833 6.99598ZM7.78673 14.9096L12.7867 11.4096L12.2133 10.5904L7.21327 14.0904L7.78673 14.9096ZM12.7817 10.5869L1.78167 3.08689L1.21833 3.91311L12.2183 11.4131L12.7817 10.5869Z"
      fill={color}
    />
  {:else}
    <path
      fill-rule="evenodd"
      clip-rule="evenodd"
      d="M7.26909 0.0565121C7.43446 -0.0295868 7.63399 -0.0165295 7.78673 0.0903855L12.7867 3.59039C12.9213 3.68457 13.001 3.83884 13 4.00308C12.999 4.16732 12.9174 4.32059 12.7817 4.41312L8.25423 7.5L12.7817 10.5869C12.9174 10.6794 12.999 10.8327 13 10.9969C13.001 11.1612 12.9213 11.3154 12.7867 11.4096L7.78673 14.9096C7.63399 15.0165 7.43446 15.0296 7.26909 14.9435C7.10373 14.8574 7 14.6864 7 14.5V8.35516L1.78167 11.9131L1.21833 11.0869L6.4791 7.5L1.21833 3.91312L1.78167 3.08689L7 6.64484V0.500001C7 0.313564 7.10373 0.142611 7.26909 0.0565121ZM8 8.53698L11.6204 11.0054L8 13.5397V8.53698ZM8 6.46302V1.46033L11.6204 3.99459L8 6.46302Z"
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
@prop export let ariaLabel = 'bluetooth';
-->
