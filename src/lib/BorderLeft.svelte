<script lang="ts">
  export let size: string = '15';
  export let role: string = 'img';
  export let color: string = 'currentColor';
  export let variation: 'solid' | 'outline' = 'outline';
  export let ariaLabel = 'border left';
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
      d="M7 1.5H8M10 1.5H11M13 1.5H14M13 4.5H14M7 4.5H8M13 7.5H14M10 7.5H11M7 7.5H8M13 10.5H14M7 10.5H8M13 13.5H14M10 13.5H11M7 13.5H8M4 13.5H5M4 7.5H5M4 1.5H5M1.5 1V14"
      stroke={color}
    />
  {:else}
    <path
      fill-rule="evenodd"
      clip-rule="evenodd"
      d="M1 14V1H2V14H1ZM5 2H4V1H5V2ZM8 2H7V1H8V2ZM11 2H10V1H11V2ZM14 2H13V1H14V2ZM8 5H7V4H8V5ZM14 5H13V4H14V5ZM5 8H4V7H5V8ZM8 8H7V7H8V8ZM11 8H10V7H11V8ZM14 8H13V7H14V8ZM8 11H7V10H8V11ZM14 11H13V10H14V11ZM5 14H4V13H5V14ZM8 14H7V13H8V14ZM11 14H10V13H11V14ZM14 14H13V13H14V14Z"
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
@prop export let ariaLabel = 'border left';
-->
