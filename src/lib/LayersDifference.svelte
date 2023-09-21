<script lang="ts">
  export let size: string = '15';
  export let role: string = 'img';
  export let color: string = 'currentColor';
  export let variation: 'solid' | 'outline' = 'outline';
  export let ariaLabel = 'layers difference';
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
      d="M4.5 4.5V1.5C4.5 0.947715 4.94772 0.5 5.5 0.5H13.5C14.0523 0.5 14.5 0.947715 14.5 1.5V9.5C14.5 10.0523 14.0523 10.5 13.5 10.5H10.5M4.5 4.5H1.5C0.947715 4.5 0.5 4.94772 0.5 5.5V13.5C0.5 14.0523 0.947716 14.5 1.5 14.5H9.5C10.0523 14.5 10.5 14.0523 10.5 13.5V10.5M4.5 4.5V7M4.5 4.5H7M10.5 10.5H8M10.5 10.5V8M8 4.5H10.5V7M4.5 8V10.5H7"
      stroke={color}
    />
  {:else}
    <path
      fill-rule="evenodd"
      clip-rule="evenodd"
      d="M4 4V1.5C4 0.671573 4.67157 0 5.5 0H13.5C14.3284 0 15 0.671573 15 1.5V9.5C15 10.3284 14.3284 11 13.5 11H11V13.5C11 14.3284 10.3284 15 9.5 15H1.5C0.671573 15 0 14.3284 0 13.5V5.5C0 4.67157 0.671573 4 1.5 4H4ZM10 5V10H5V5H10Z"
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
@prop export let ariaLabel = 'layers difference';
-->
