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
  export let ariaLabel = 'paw';
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
      d="M6.5 3V2C6.5 1.17157 5.82843 0.5 5 0.5C4.17157 0.5 3.5 1.17157 3.5 2V3C3.5 3.82843 4.17157 4.5 5 4.5C5.82843 4.5 6.5 3.82843 6.5 3Z"
      stroke={color}
    />
    <path
      d="M11.5 3V2C11.5 1.17157 10.8284 0.5 10 0.5C9.17157 0.5 8.5 1.17157 8.5 2V3C8.5 3.82843 9.17157 4.5 10 4.5C10.8284 4.5 11.5 3.82843 11.5 3Z"
      stroke={color}
    />
    <path
      d="M14.5 7.5V7C14.5 6.17157 13.8284 5.5 13 5.5C12.1716 5.5 11.5 6.17157 11.5 7V7.5C11.5 8.32843 12.1716 9 13 9C13.8284 9 14.5 8.32843 14.5 7.5Z"
      stroke={color}
    />
    <path
      d="M3.5 7.5V7C3.5 6.17157 2.82843 5.5 2 5.5C1.17157 5.5 0.5 6.17157 0.5 7V7.5C0.5 8.32843 1.17157 9 2 9C2.82843 9 3.5 8.32843 3.5 7.5Z"
      stroke={color}
    />
    <path
      d="M2.8554 11.6399L5.77324 8.09678C6.66803 7.01025 8.33197 7.01025 9.22676 8.09678L12.1446 11.6399C13.084 12.7806 12.2726 14.5 10.7948 14.5C10.6009 14.5 10.4097 14.4549 10.2363 14.3681L9.87662 14.1883C8.3805 13.4403 6.6195 13.4403 5.12338 14.1883L4.76371 14.3681C4.59029 14.4549 4.39905 14.5 4.20516 14.5C2.72742 14.5 1.91599 12.7806 2.8554 11.6399Z"
      stroke={color}
    />
  {:else}
    <path
      d="M5 0C3.89543 0 3 0.895431 3 2V3C3 4.10457 3.89543 5 5 5C6.10457 5 7 4.10457 7 3V2C7 0.895431 6.10457 0 5 0Z"
      fill={color}
    />
    <path
      d="M10 0C8.89543 0 8 0.895431 8 2V3C8 4.10457 8.89543 5 10 5C11.1046 5 12 4.10457 12 3V2C12 0.895431 11.1046 0 10 0Z"
      fill={color}
    />
    <path
      d="M2 5C0.895431 5 0 5.89543 0 7V7.5C0 8.60457 0.895431 9.5 2 9.5C3.10457 9.5 4 8.60457 4 7.5V7C4 5.89543 3.10457 5 2 5Z"
      fill={color}
    />
    <path
      d="M13 5C11.8954 5 11 5.89543 11 7V7.5C11 8.60457 11.8954 9.5 13 9.5C14.1046 9.5 15 8.60457 15 7.5V7C15 5.89543 14.1046 5 13 5Z"
      fill={color}
    />
    <path
      d="M9.61273 7.77893C8.51793 6.44953 6.48207 6.44953 5.38727 7.77893L2.46943 11.322C1.2614 12.7889 2.30486 15 4.20516 15C4.47668 15 4.74447 14.9368 4.98732 14.8154L5.34699 14.6355C6.70234 13.9578 8.29766 13.9578 9.65301 14.6355L10.0127 14.8154C10.2555 14.9368 10.5233 15 10.7948 15C12.6951 15 13.7386 12.7889 12.5306 11.322L9.61273 7.77893Z"
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
@prop export let ariaLabel = 'paw';
-->
