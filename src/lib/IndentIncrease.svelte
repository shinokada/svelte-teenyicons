<script lang="ts">
  export let size: string = '15';
  export let role: string = 'img';
  export let color: string = 'currentColor';
  export let variation: 'solid' | 'outline' = 'outline';
  export let ariaLabel = 'indent increase';
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
      d="M2.5 7.5L2.85355 7.85355C3.04882 7.65829 3.04882 7.34171 2.85355 7.14645L2.5 7.5ZM3 4H15V3H3V4ZM7 8H15V7H7V8ZM3 12H15V11H3V12ZM0.853553 9.85355L2.85355 7.85355L2.14645 7.14645L0.146447 9.14645L0.853553 9.85355ZM2.85355 7.14645L0.853553 5.14645L0.146447 5.85355L2.14645 7.85355L2.85355 7.14645Z"
      fill={color}
    />
  {:else}
    <path
      fill-rule="evenodd"
      clip-rule="evenodd"
      d="M15 4H3V3H15V4ZM0.853553 5.14645L2.85355 7.14645C3.04882 7.34171 3.04882 7.65829 2.85355 7.85355L0.853553 9.85355L0.146446 9.14645L1.79289 7.5L0.146446 5.85355L0.853553 5.14645ZM15 8H7V7H15V8ZM15 12H3V11H15V12Z"
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
@prop export let ariaLabel = 'indent increase';
-->
