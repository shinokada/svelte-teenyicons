<script lang="ts">
  export let size: string = '15';
  export let role: string = 'img';
  export let color: string = 'currentColor';
  export let variation: 'solid' | 'outline' = 'outline';
  export let ariaLabel = 'battery 0';
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
      d="M14.5 10L14.5 5M12.5 11.5V3.5C12.5 2.94772 12.0523 2.5 11.5 2.5L1.5 2.5C0.947715 2.5 0.5 2.94772 0.5 3.5L0.5 11.5C0.5 12.0523 0.947715 12.5 1.5 12.5H11.5C12.0523 12.5 12.5 12.0523 12.5 11.5Z"
      stroke={color}
    />
  {:else}
    <path
      d="M1.5 13C0.671573 13 0 12.3284 0 11.5V3.5C0 2.67157 0.671572 2 1.5 2H11.5C12.3284 2 13 2.67157 13 3.5V11.5C13 12.3284 12.3284 13 11.5 13L1.5 13Z"
      fill={color}
    /> <path d="M15 10V5H14V10H15Z" fill={color} />
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
@prop export let ariaLabel = 'battery 0';
-->
