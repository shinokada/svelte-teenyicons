<script lang="ts">
  export let size: string = '15';
  export let role: string = 'img';
  export let color: string = 'currentColor';
  export let variation: 'solid' | 'outline' = 'outline';
  export let ariaLabel = 'adjust vertical';
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
      d="M7.5 12.5V15M12.5 6.55671e-07V2.5M2.5 6.55671e-07L2.50001 6.5M2.5 8.5V15M7.5 10.5V0M12.5 4.5V15M10.5 4.5H14.5V2.5H10.5V4.5ZM5.5 12.5H9.5V10.5H5.5V12.5ZM0.5 8.5H4.5V6.5H0.5V8.5Z"
      stroke={color}
    />
  {:else}
    <path d="M2 0L2.00001 6H0V9H2V15H3V9H5V6H3.00001L3 0H2Z" fill={color} />
    <path d="M5 10H7V0H8V10H10V13H8V15H7V13H5V10Z" fill={color} />
    <path d="M12 0V2H10V5H12V15H13V5H15V2H13V0H12Z" fill={color} />
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
@prop export let ariaLabel = 'adjust vertical';
-->
