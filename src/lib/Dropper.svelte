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
  export let ariaLabel = 'dropper';
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
      d="M0.5 12.5L0.146447 12.1465L0 12.2929V12.5H0.5ZM8 5L8.35355 4.64645C8.15829 4.45119 7.84171 4.45119 7.64645 4.64645L8 5ZM10 7L10.3536 7.35356C10.5488 7.1583 10.5488 6.84171 10.3536 6.64645L10 7ZM2.5 14.5V15H2.70711L2.85355 14.8536L2.5 14.5ZM0.5 14.5H0C0 14.7761 0.223858 15 0.5 15L0.5 14.5ZM7.5 4.5L7.14645 4.14645L6.79289 4.5L7.14645 4.85356L7.5 4.5ZM10.5858 1.41422L10.2322 1.06066L10.5858 1.41422ZM13.4142 1.41422L13.0607 1.76777L13.0607 1.76777L13.4142 1.41422ZM13.5858 1.58579L13.9393 1.23224L13.9393 1.23224L13.5858 1.58579ZM13.5858 4.41422L13.2322 4.06066L13.5858 4.41422ZM10.5 7.5L10.1464 7.85356L10.5 8.20711L10.8536 7.85356L10.5 7.5ZM0.853553 12.8536L8.35355 5.35356L7.64645 4.64645L0.146447 12.1465L0.853553 12.8536ZM7.64645 5.35356L9.64645 7.35356L10.3536 6.64645L8.35355 4.64645L7.64645 5.35356ZM9.64645 6.64645L2.14645 14.1465L2.85355 14.8536L10.3536 7.35356L9.64645 6.64645ZM2.5 14H0.5V15H2.5V14ZM1 14.5V12.5H0V14.5H1ZM6.14645 3.85356L11.1464 8.85356L11.8536 8.14645L6.85355 3.14645L6.14645 3.85356ZM7.85355 4.85356L10.9393 1.76777L10.2322 1.06066L7.14645 4.14645L7.85355 4.85356ZM13.0607 1.76777L13.2322 1.93934L13.9393 1.23224L13.7678 1.06066L13.0607 1.76777ZM13.2322 4.06066L10.1464 7.14645L10.8536 7.85356L13.9393 4.76777L13.2322 4.06066ZM10.8536 7.14645L7.85355 4.14645L7.14645 4.85356L10.1464 7.85356L10.8536 7.14645ZM13.2322 1.93934C13.818 2.52513 13.818 3.47488 13.2322 4.06066L13.9393 4.76777C14.9157 3.79146 14.9156 2.20855 13.9393 1.23224L13.2322 1.93934ZM10.9393 1.76777C11.5251 1.18198 12.4749 1.18198 13.0607 1.76777L13.7678 1.06066C12.7915 0.0843534 11.2085 0.0843515 10.2322 1.06066L10.9393 1.76777Z"
      fill={color}
    />
  {:else}
    <path
      d="M13.7678 1.06066C12.7915 0.0843534 11.2086 0.0843515 10.2323 1.06066L7.50007 3.7929L6.85359 3.14642L6.14648 3.85353L11.1465 8.85353L11.8536 8.14642L11.2072 7.50001L13.9394 4.76777C14.9157 3.79146 14.9157 2.20855 13.9394 1.23224L13.7678 1.06066Z"
      fill={color}
    />
    <path
      d="M6.14645 6.14645C6.34171 5.95118 6.65829 5.95118 6.85355 6.14645L8.85355 8.14645C9.04882 8.34171 9.04882 8.65829 8.85355 8.85355L2.70711 15H0.5C0.223858 15 0 14.7761 0 14.5V12.2929L6.14645 6.14645Z"
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
@prop export let ariaLabel = 'dropper';
-->
