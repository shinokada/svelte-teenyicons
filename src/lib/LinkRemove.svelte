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
  export let ariaLabel = 'link remove';
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
      d="M4.5 6.5L1.32843 9.67157C0.797994 10.202 0.5 10.9214 0.5 11.6716C0.5 13.2337 1.76633 14.5 3.32843 14.5C4.07857 14.5 4.79799 14.202 5.32843 13.6716L8.5 10.5M10.5 8.5L13.6716 5.32843C14.202 4.79799 14.5 4.07857 14.5 3.32843C14.5 1.76633 13.2337 0.5 11.6716 0.5C10.9214 0.5 10.202 0.797993 9.67157 1.32843L6.5 4.5M4.5 10.5L10.5 4.5M3 4.5H0M4.5 0V3M10.5 12V15M12 10.5H15"
      stroke={color}
    />
  {:else}
    <path
      fill-rule="evenodd"
      clip-rule="evenodd"
      d="M4 3V0H5V3H4ZM9.31802 0.974873C9.94222 0.350672 10.7888 0 11.6716 0C13.5098 0 15 1.49019 15 3.32843C15 4.21118 14.6493 5.05778 14.0251 5.68198L10.8536 8.85355L10.1464 8.14645L13.318 4.97487C13.7547 4.53821 14 3.94596 14 3.32843C14 2.04247 12.9575 1 11.6716 1C11.054 1 10.4618 1.24532 10.0251 1.68198L6.85355 4.85355L6.14645 4.14645L9.31802 0.974873ZM0 4H3V5H0V4ZM10.8536 4.85355L4.85355 10.8536L4.14645 10.1464L10.1464 4.14645L10.8536 4.85355ZM4.85355 6.85355L1.68198 10.0251C1.24532 10.4618 1 11.054 1 11.6716C1 12.9575 2.04247 14 3.32843 14C3.94596 14 4.53821 13.7547 4.97487 13.318L8.14645 10.1464L8.85355 10.8536L5.68198 14.0251C5.05778 14.6493 4.21118 15 3.32843 15C1.49019 15 0 13.5098 0 11.6716C0 10.7888 0.350673 9.94222 0.974874 9.31802L4.14645 6.14645L4.85355 6.85355ZM15 11H12V10H15V11ZM10 15V12H11V15H10Z"
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
@prop export let ariaLabel = 'link remove';
-->
