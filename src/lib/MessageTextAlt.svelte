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
  export let ariaLabel = 'message text alt';
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
      d="M3.5 11.4928H4V10.9928H3.5V11.4928ZM3.5 14.4908H3C3 14.6802 3.10697 14.8533 3.27632 14.938C3.44568 15.0227 3.64835 15.0045 3.79988 14.8909L3.5 14.4908ZM7.5 11.4928V10.9928H7.33342L7.20013 11.0927L7.5 11.4928ZM4.5 3.99738H4V4.99738H4.5V3.99738ZM10.5 4.99738H11V3.99738H10.5V4.99738ZM4.5 6.99542H4V7.99542H4.5V6.99542ZM8.5 7.99542H9V6.99542H8.5V7.99542ZM3 11.4928V14.4908H4V11.4928H3ZM3.79988 14.8909L7.79987 11.8929L7.20013 11.0927L3.20012 14.0908L3.79988 14.8909ZM7.5 11.9928H13.5V10.9928H7.5V11.9928ZM13.5 11.9928C14.3288 11.9928 15 11.3226 15 10.4935H14C14 10.7696 13.7772 10.9928 13.5 10.9928V11.9928ZM15 10.4935V1.49933H14V10.4935H15ZM15 1.49933C15 0.670226 14.3288 0 13.5 0V1C13.7772 1 14 1.22315 14 1.49933H15ZM13.5 0H1.5V1H13.5V0ZM1.5 0C0.671178 0 0 0.670226 0 1.49933H1C1 1.22315 1.22282 1 1.5 1V0ZM0 1.49933V10.4935H1V1.49933H0ZM0 10.4935C0 11.3226 0.671178 11.9928 1.5 11.9928V10.9928C1.22282 10.9928 1 10.7696 1 10.4935H0ZM1.5 11.9928H3.5V10.9928H1.5V11.9928ZM4.5 4.99738H10.5V3.99738H4.5V4.99738ZM4.5 7.99542H8.5V6.99542H4.5V7.99542Z"
      fill={color}
    />
  {:else}
    <path
      fill-rule="evenodd"
      clip-rule="evenodd"
      d="M0 1.49933C0 0.670226 0.671178 0 1.5 0H13.5C14.3288 0 15 0.670226 15 1.49933V10.4935C15 11.3226 14.3288 11.9928 13.5 11.9928H7.66658L3.79988 14.8909C3.64835 15.0045 3.44568 15.0227 3.27632 14.938C3.10697 14.8533 3 14.6802 3 14.4908V11.9928H1.5C0.671178 11.9928 0 11.3226 0 10.4935V1.49933ZM4 3.99738H11V4.99738H4V3.99738ZM4 6.99542H9V7.99542H4V6.99542Z"
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
@prop export let ariaLabel = 'message text alt';
-->
