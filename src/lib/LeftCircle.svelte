<script lang="ts">
  export let size: string = '15';
  export let role: string = 'img';
  export let color: string = 'currentColor';
  export let variation: 'solid' | 'outline' = 'outline';
  export let ariaLabel = 'left circle';
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
      d="M8.85356 4.85355L9.20711 4.5L8.5 3.79289L8.14645 4.14644L8.85356 4.85355ZM5.5 7.5L5.14645 7.14644L4.79289 7.5L5.14645 7.85355L5.5 7.5ZM8.14645 10.8536L8.5 11.2071L9.20711 10.5L8.85355 10.1464L8.14645 10.8536ZM8.14645 4.14644L5.14645 7.14644L5.85355 7.85355L8.85356 4.85355L8.14645 4.14644ZM5.14645 7.85355L8.14645 10.8536L8.85355 10.1464L5.85355 7.14644L5.14645 7.85355ZM7.5 14C3.91015 14 0.999999 11.0898 1 7.5H0C-7.15256e-07 11.6421 3.35786 15 7.5 15V14ZM14 7.5C14 11.0899 11.0898 14 7.5 14V15C11.6421 15 15 11.6421 15 7.5H14ZM7.5 1C11.0899 1 14 3.91015 14 7.5H15C15 3.35787 11.6421 7.15256e-07 7.5 0V1ZM7.5 0C3.35787 -7.15256e-07 7.15256e-07 3.35786 0 7.5H1C1 3.91015 3.91015 0.999999 7.5 1V0Z"
      fill={color}
    />
  {:else}
    <path
      fill-rule="evenodd"
      clip-rule="evenodd"
      d="M0 7.5C0 3.35786 3.35786 0 7.5 0C11.6421 2.03558e-06 15 3.35787 15 7.5C15 11.6421 11.6421 15 7.5 15C3.35786 15 -2.03557e-06 11.6421 0 7.5ZM9.00007 11.7072L4.79297 7.50007L9.00008 3.29297L9.00007 11.7072Z"
      fill={color}
    />
  {/if}
</svg>

<!--
@component
[Go to docs](https://svelte-teenyicons.vercel.app/)
## Props
@prop export let size: string = '15';
@prop export let role: string = 'img';
@prop export let color: string = 'currentColor';
@prop export let variation: 'solid' | 'outline' = 'outline';
@prop export let ariaLabel = 'left circle';
-->
