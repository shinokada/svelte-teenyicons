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
  export let ariaLabel = 'wan';
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
      d="M3.5 14.5L3.0111 14.6048C3.05879 14.8273 3.25077 14.9896 3.47816 14.9995C3.70554 15.0095 3.91095 14.8646 3.97789 14.647L3.5 14.5ZM7.5 1.5L7.97789 1.35296C7.91334 1.14316 7.7195 1 7.5 1C7.2805 1 7.08666 1.14316 7.02211 1.35296L7.5 1.5ZM11.5 14.5L11.0221 14.647C11.089 14.8646 11.2945 15.0095 11.5218 14.9995C11.7492 14.9896 11.9412 14.8273 11.9889 14.6048L11.5 14.5ZM0.0110988 0.604765L3.0111 14.6048L3.9889 14.3952L0.988901 0.395235L0.0110988 0.604765ZM3.97789 14.647L7.97789 1.64704L7.02211 1.35296L3.02211 14.353L3.97789 14.647ZM7.02211 1.64704L11.0221 14.647L11.9779 14.353L7.97789 1.35296L7.02211 1.64704ZM11.9889 14.6048L14.9889 0.604765L14.0111 0.395235L11.0111 14.3952L11.9889 14.6048ZM0 6H15V5H0V6ZM0 10H15V9H0V10Z"
      fill={color}
    />
  {:else}
    <path
      fill-rule="evenodd"
      clip-rule="evenodd"
      d="M0.952935 5L0.0110988 0.604762L0.988901 0.395233L1.97564 5H5.89994L7.02211 1.35295C7.08666 1.14316 7.2805 0.999998 7.5 0.999998C7.7195 0.999998 7.91334 1.14316 7.97789 1.35295L9.10006 5H13.0244L14.0111 0.395233L14.9889 0.604762L14.0471 5H15V6H13.8328L13.1899 9H15V10H12.9756L11.9889 14.6048C11.9412 14.8273 11.7492 14.9896 11.5218 14.9995C11.2945 15.0095 11.089 14.8646 11.0221 14.647L9.59225 10H5.40775L3.97789 14.647C3.91095 14.8646 3.70554 15.0095 3.47816 14.9995C3.25077 14.9896 3.05879 14.8273 3.0111 14.6048L2.02436 10H0V9H1.81008L1.16722 6H0V5H0.952935ZM2.18992 6L2.83278 9H4.66917L5.59225 6H2.18992ZM6.63852 6L5.71544 9H9.28456L8.36148 6H6.63852ZM8.05379 5L7.5 3.20018L6.94621 5H8.05379ZM9.40775 6L10.3308 9H12.1672L12.8101 6H9.40775ZM11.9529 10H10.6385L11.4133 12.5181L11.9529 10ZM4.36148 10H3.04707L3.58667 12.5181L4.36148 10Z"
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
@prop export let ariaLabel = 'wan';
-->
