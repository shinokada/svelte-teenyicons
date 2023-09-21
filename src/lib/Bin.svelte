<script lang="ts">
  export let size: string = '15';
  export let role: string = 'img';
  export let color: string = 'currentColor';
  export let variation: 'solid' | 'outline' = 'outline';
  export let ariaLabel = 'bin';
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
      d="M4.5 3V1.5C4.5 0.947715 4.94772 0.5 5.5 0.5H9.5C10.0523 0.5 10.5 0.947715 10.5 1.5V3M0 3.5H15M1.5 3.5V13.5C1.5 14.0523 1.94772 14.5 2.5 14.5H12.5C13.0523 14.5 13.5 14.0523 13.5 13.5V3.5M7.5 7V12M4.5 9V12M10.5 9V12"
      stroke={color}
    />
  {:else}
    <path
      fill-rule="evenodd"
      clip-rule="evenodd"
      d="M11 3V1.5C11 0.671573 10.3284 0 9.5 0H5.5C4.67157 0 4 0.671573 4 1.5V3H0V4H1V13.5C1 14.3284 1.67157 15 2.5 15H12.5C13.3284 15 14 14.3284 14 13.5V4H15V3H11ZM5 1.5C5 1.22386 5.22386 1 5.5 1H9.5C9.77614 1 10 1.22386 10 1.5V3H5V1.5ZM7 7V12H8V7H7ZM4 12V9H5V12H4ZM10 9V12H11V9H10Z"
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
@prop export let ariaLabel = 'bin';
-->
