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
  export let ariaLabel = 'image document';
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
      d="M13.5 3.5H14V3.29289L13.8536 3.14645L13.5 3.5ZM10.5 0.5L10.8536 0.146447L10.7071 0H10.5V0.5ZM11.5 8.49543L11.854 8.14228L11.5005 7.78804L11.1466 8.14176L11.5 8.49543ZM8.5 11.4935L8.10976 11.8061L8.45868 12.2416L8.85344 11.8471L8.5 11.4935ZM4.5 6.5L4.89024 6.1874L4.48699 5.68401L4.1 6.2L4.5 6.5ZM12.5 14H2.5V15H12.5V14ZM2 13.5V1.5H1V13.5H2ZM13 3.5V13.5H14V3.5H13ZM2.5 1H10.5V0H2.5V1ZM10.1464 0.853553L13.1464 3.85355L13.8536 3.14645L10.8536 0.146447L10.1464 0.853553ZM2.5 14C2.22386 14 2 13.7761 2 13.5H1C1 14.3284 1.67157 15 2.5 15V14ZM12.5 15C13.3284 15 14 14.3284 14 13.5H13C13 13.7761 12.7761 14 12.5 14V15ZM2 1.5C2 1.22386 2.22386 1 2.5 1V0C1.67157 0 1 0.671574 1 1.5H2ZM10 6H11V5H10V6ZM13.854 10.1469L11.854 8.14228L11.146 8.84858L13.146 10.8531L13.854 10.1469ZM11.1466 8.14176L8.14656 11.1398L8.85344 11.8471L11.8534 8.8491L11.1466 8.14176ZM8.89024 11.1809L4.89024 6.1874L4.10976 6.8126L8.10976 11.8061L8.89024 11.1809ZM4.1 6.2L1.1 10.2L1.9 10.8L4.9 6.8L4.1 6.2Z"
      fill={color}
    />
  {:else}
    <path
      fill-rule="evenodd"
      clip-rule="evenodd"
      d="M1 1.5C1 0.671573 1.67157 0 2.5 0H10.7071L14 3.29289V10.2916L11.5004 7.78819L8.54137 10.7453L4.4998 5.69995L1 10.0747V1.5ZM11 6H10V5H11V6Z"
      fill={color}
    />
    <path
      d="M1 11.6755V13.5C1 14.3284 1.67157 15 2.5 15H12.5C13.3284 15 14 14.3284 14 13.5V11.7069L11.4997 9.20271L8.45873 12.2417L4.50031 7.3001L1 11.6755Z"
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
@prop export let ariaLabel = 'image document';
-->
