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
  export let ariaLabel = 'slack';
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
      d="M10.5 7.5V6C10.5 5.17157 11.1716 4.5 12 4.5C12.8284 4.5 13.5 5.17157 13.5 6C13.5 6.82843 12.8284 7.5 12 7.5H10.5ZM10.5 7.5H7.5M10.5 7.5V2C10.5 1.17157 9.82843 0.5 9 0.5C8.17157 0.5 7.5 1.17157 7.5 2V7.5M7.5 7.5V4.5M7.5 7.5H2C1.17157 7.5 0.5 6.82843 0.5 6C0.5 5.17157 1.17157 4.5 2 4.5H7.5M7.5 7.5H13C13.8284 7.5 14.5 8.17157 14.5 9C14.5 9.82843 13.8284 10.5 13 10.5H7.5M7.5 7.5V10.5M7.5 7.5H4.5M7.5 7.5V13C7.5 13.8284 6.82843 14.5 6 14.5C5.17157 14.5 4.5 13.8284 4.5 13V7.5M7.5 4.5V3C7.5 2.17157 6.82843 1.5 6 1.5C5.17157 1.5 4.5 2.17157 4.5 3C4.5 3.82843 5.17157 4.5 6 4.5H7.5ZM7.5 10.5H9C9.82843 10.5 10.5 11.1716 10.5 12C10.5 12.8284 9.82843 13.5 9 13.5C8.17157 13.5 7.5 12.8284 7.5 12V10.5ZM4.5 7.5V9C4.5 9.82843 3.82843 10.5 3 10.5C2.17157 10.5 1.5 9.82843 1.5 9C1.5 8.17157 2.17157 7.5 3 7.5H4.5Z"
      stroke={color}
    />
  {:else}
    <path
      d="M10.3846 6.92308H8.07692V1.15385C8.07692 0.516595 8.59352 0 9.23077 0C9.86802 0 10.3846 0.516595 10.3846 1.15385V6.92308Z"
      fill={color}
    />
    <path
      d="M12.6923 6.92308H11.5385V5.76923C11.5385 5.13198 12.0551 4.61539 12.6923 4.61539C13.3296 4.61539 13.8462 5.13198 13.8462 5.76923C13.8462 6.40648 13.3296 6.92308 12.6923 6.92308Z"
      fill={color}
    />
    <path
      d="M13.8462 8.07692H8.07692V10.3846H13.8462C14.4834 10.3846 15 9.86802 15 9.23077C15 8.59352 14.4834 8.07692 13.8462 8.07692Z"
      fill={color}
    />
    <path
      d="M8.07692 12.6923V11.5385H9.23077C9.86802 11.5385 10.3846 12.0551 10.3846 12.6923C10.3846 13.3296 9.86802 13.8462 9.23077 13.8462C8.59352 13.8462 8.07692 13.3296 8.07692 12.6923Z"
      fill={color}
    />
    <path
      d="M1.15385 4.61539H6.92308V6.92308H1.15385C0.516595 6.92308 0 6.40648 0 5.76923C0 5.13198 0.516595 4.61539 1.15385 4.61539Z"
      fill={color}
    />
    <path
      d="M6.92308 2.30769V3.46154H5.76923C5.13198 3.46154 4.61539 2.94494 4.61539 2.30769C4.61539 1.67044 5.13198 1.15385 5.76923 1.15385C6.40648 1.15385 6.92308 1.67044 6.92308 2.30769Z"
      fill={color}
    />
    <path
      d="M1.15385 9.23077C1.15385 8.59352 1.67044 8.07692 2.30769 8.07692H3.46154V9.23077C3.46154 9.86802 2.94494 10.3846 2.30769 10.3846C1.67044 10.3846 1.15385 9.86802 1.15385 9.23077Z"
      fill={color}
    />
    <path
      d="M4.61539 13.8462V8.07692H6.92308V13.8462C6.92308 14.4834 6.40648 15 5.76923 15C5.13198 15 4.61539 14.4834 4.61539 13.8462Z"
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
@prop export let ariaLabel = 'slack';
-->
