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
  export let ariaLabel = 'n64';
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
      d="M4.5 4V7M3 5.5H6M9 5.5H10M11 6.5H12M4.5 2.5H3.5C1.84315 2.5 0.5 3.84315 0.5 5.5V10.3377C0.5 10.9796 1.02037 11.5 1.66228 11.5C2.16256 11.5 2.60671 11.1799 2.76491 10.7053L3.5 8.5H4.59501C5.10876 8.5 5.53893 8.88929 5.59005 9.4005L5.85074 12.0074C5.93547 12.8548 6.64847 13.5 7.5 13.5C8.35153 13.5 9.06452 12.8548 9.14926 12.0074L9.40995 9.4005C9.46107 8.8893 9.89124 8.5 10.405 8.5H11.5L12.2351 10.7053C12.3933 11.1799 12.8374 11.5 13.3377 11.5C13.9796 11.5 14.5 10.9796 14.5 10.3377V5.5C14.5 3.84315 13.1569 2.5 11.5 2.5H10.5L9.5 1.5H5.5L4.5 2.5Z"
      stroke={color}
    />
  {:else}
    <path
      fill-rule="evenodd"
      clip-rule="evenodd"
      d="M5.29289 1H9.70711L10.7071 2H11.5C13.433 2 15 3.567 15 5.5V10.3377C15 11.2558 14.2558 12 13.3377 12C12.6222 12 11.987 11.5422 11.7607 10.8634L11.1396 9H10.405C10.1481 9 9.93303 9.19465 9.90747 9.45025L9.64677 12.0572C9.53648 13.1601 8.60841 14 7.5 14C6.39159 14 5.46352 13.1601 5.35323 12.0572L5.09253 9.45025C5.06697 9.19465 4.85189 9 4.59501 9H3.86038L3.23925 10.8634C3.01299 11.5422 2.37777 12 1.66228 12C0.744227 12 0 11.2558 0 10.3377V5.5C0 3.567 1.567 2 3.5 2H4.29289L5.29289 1ZM4 7V6H3V5H4V4H5V5H6V6H5V7H4ZM9 6H10V5H9V6ZM12 6V7H11V6H12Z"
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
@prop export let ariaLabel = 'n64';
-->
