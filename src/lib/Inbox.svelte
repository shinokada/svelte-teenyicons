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
  export let ariaLabel = 'inbox';
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
      d="M7.71261 11.4926L7.67769 10.9938L7.71261 11.4926ZM1.5 1H13.5V0H1.5V1ZM14 1.5V13.5H15V1.5H14ZM13.5 14H1.5V15H13.5V14ZM1 13.5V1.5H0V13.5H1ZM1.5 14C1.22386 14 1 13.7761 1 13.5H0C0 14.3284 0.671573 15 1.5 15V14ZM14 13.5C14 13.7761 13.7761 14 13.5 14V15C14.3284 15 15 14.3284 15 13.5H14ZM13.5 1C13.7761 1 14 1.22386 14 1.5H15C15 0.671573 14.3284 0 13.5 0V1ZM1.5 0C0.671573 0 0 0.671574 0 1.5H1C1 1.22386 1.22386 1 1.5 1V0ZM7.5 12C7.58314 12 7.66569 11.9971 7.74753 11.9914L7.67769 10.9938C7.61907 10.9979 7.55982 11 7.5 11V12ZM6.67656 11.9025C6.94113 11.9663 7.21696 12 7.5 12V11C7.29657 11 7.09945 10.9758 6.91111 10.9304L6.67656 11.9025ZM6.91111 10.9304C5.94219 10.6966 5.01155 10.0349 3.94125 9.34386C2.92423 8.68718 1.77112 8 0.5 8V9C1.43802 9 2.35807 9.51196 3.39881 10.184C4.38625 10.8215 5.49796 11.6181 6.67656 11.9025L6.91111 10.9304ZM7.74753 11.9914C9.13355 11.8943 10.4475 11.0637 11.6128 10.359C12.8421 9.61562 13.9219 9 15 9V8C13.5928 8 12.2685 8.79387 11.0953 9.50334C9.85794 10.2516 8.77088 10.9173 7.67769 10.9938L7.74753 11.9914Z"
      fill={color}
    />
  {:else}
    <path
      d="M0 1.5C0 0.671573 0.671573 0 1.5 0H13.5C14.3284 0 15 0.671573 15 1.5V8H10.5C10.2239 8 10 8.22386 10 8.5C10 9.88071 8.88071 11 7.5 11C6.11929 11 5 9.88071 5 8.5C5 8.22386 4.77614 8 4.5 8H0V1.5Z"
      fill={color}
    />
    <path
      d="M0 9V13.5C0 14.3284 0.671573 15 1.5 15H13.5C14.3284 15 15 14.3284 15 13.5V9H10.9646C10.7219 10.6961 9.26324 12 7.5 12C5.73676 12 4.27806 10.6961 4.03544 9H0Z"
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
@prop export let ariaLabel = 'inbox';
-->
