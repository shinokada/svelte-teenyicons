<script lang="ts">
  export let size: string = '15';
  export let role: string = 'img';
  export let color: string = 'currentColor';
  export let variation: 'solid' | 'outline' = 'outline';
  export let ariaLabel = 'adjust horizontal alt';
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
      d="M15 3.5L6.5 3.5M6.5 3.5C6.5 2.39543 5.60457 1.5 4.5 1.5C3.39543 1.5 2.5 2.39543 2.5 3.5M6.5 3.5C6.5 4.60457 5.60457 5.5 4.5 5.5C3.39543 5.5 2.5 4.60457 2.5 3.5M2.5 3.5L0 3.5M15 11.5L12.5 11.5M12.5 11.5C12.5 10.3954 11.6046 9.5 10.5 9.5C9.39543 9.5 8.5 10.3954 8.5 11.5M12.5 11.5C12.5 12.6046 11.6046 13.5 10.5 13.5C9.39543 13.5 8.5 12.6046 8.5 11.5M8.5 11.5H1.27146e-07"
      stroke={color}
    />
  {:else}
    <path
      d="M4.5 1C3.29052 1 2.28165 1.85888 2.05001 3L3.21071e-06 3L3.167e-06 4H2.05001C2.28165 5.14112 3.29052 6 4.5 6C5.70948 6 6.71836 5.14112 6.94999 4L15 4V3L6.94999 3C6.71836 1.85888 5.70948 1 4.5 1Z"
      fill={color}
    />
    <path
      d="M10.5 9C9.29053 9 8.28165 9.85888 8.05001 11H2.86102e-06L3.77099e-06 12H8.05001C8.28165 13.1411 9.29052 14 10.5 14C11.7095 14 12.7184 13.1411 12.95 12L15 12V11L12.95 11C12.7184 9.85888 11.7095 9 10.5 9Z"
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
@prop export let ariaLabel = 'adjust horizontal alt';
-->
