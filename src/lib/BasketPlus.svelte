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
  export let ariaLabel = 'basket plus';
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
      d="M2.44898 14.398L2.89619 14.1743L2.89619 14.1743L2.44898 14.398ZM12.551 14.398L12.9982 14.6216L12.9982 14.6216L12.551 14.398ZM0.703196 6H14.2968V5H0.703196V6ZM14 5.7032V6.14196H15V5.7032H14ZM12.3859 14H2.61409V15H12.3859V14ZM1 6.14196V5.7032H0V6.14196H1ZM2.89619 14.1743C1.6492 11.6804 1 8.93031 1 6.14196H0C0 9.08555 0.685346 11.9887 2.00176 14.6216L2.89619 14.1743ZM2.61409 14C2.73356 14 2.84277 14.0675 2.89619 14.1743L2.00176 14.6216C2.11773 14.8535 2.35478 15 2.61409 15V14ZM12.1038 14.1743C12.1572 14.0675 12.2664 14 12.3859 14V15C12.6452 15 12.8823 14.8535 12.9982 14.6216L12.1038 14.1743ZM14 6.14196C14 8.93031 13.3508 11.6804 12.1038 14.1743L12.9982 14.6216C14.3147 11.9887 15 9.08555 15 6.14196H14ZM14.2968 6C14.1329 6 14 5.86712 14 5.7032H15C15 5.31483 14.6852 5 14.2968 5V6ZM0.703196 5C0.314831 5 0 5.31483 0 5.7032H1C1 5.86712 0.867117 6 0.703196 6V5ZM3.92875 5.75725L6.92875 0.757248L6.07125 0.242752L3.07125 5.24275L3.92875 5.75725ZM8.07125 0.757248L11.0713 5.75725L11.9287 5.24275L8.92875 0.242752L8.07125 0.757248ZM7 7V12H8V7H7ZM5 10H10V9H5V10Z"
      fill={color}
    />
  {:else}
    <path
      fill-rule="evenodd"
      clip-rule="evenodd"
      d="M4.38313 4.99998L6.92878 0.757233L6.07129 0.242737L3.21694 4.99998H0.703196C0.314831 4.99998 0 5.31482 0 5.70318V6.14194C0 9.08554 0.685346 11.9887 2.00176 14.6215C2.11773 14.8535 2.35478 15 2.61409 15H12.3859C12.6452 15 12.8823 14.8535 12.9982 14.6215C14.3147 11.9887 15 9.08554 15 6.14194V5.70318C15 5.31482 14.6852 4.99998 14.2968 4.99998H11.7831L8.92878 0.242737L8.07129 0.757233L10.6169 4.99998H4.38313ZM7 12V9.99998H5V8.99998H7V6.99998H8V8.99998H10V9.99998H8V12H7Z"
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
@prop export let ariaLabel = 'basket plus';
-->
