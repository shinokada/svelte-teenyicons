<script lang="ts">
  export let size: string = '15';
  export let role: string = 'img';
  export let color: string = 'currentColor';
  export let variation: 'solid' | 'outline' = 'outline';
  export let ariaLabel = 'hourglass';
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
      d="M3.5 0V4.67157C3.5 5.20201 3.71071 5.71071 4.08579 6.08579L4.79289 6.79289C5.18342 7.18342 5.18342 7.81658 4.79289 8.20711L3.79289 9.20711C3.60536 9.39464 3.5 9.649 3.5 9.91421V15M11.5 0V5.08579C11.5 5.351 11.3946 5.60536 11.2071 5.79289L10.2071 6.79289C9.81658 7.18342 9.81658 7.81658 10.2071 8.20711L11.2071 9.20711C11.3946 9.39464 11.5 9.649 11.5 9.91421V15M1 0.5H14M1 14.5H14"
      stroke={color}
    />
  {:else}
    <path
      fill-rule="evenodd"
      clip-rule="evenodd"
      d="M12.0001 1H14V0H1V1H3V4.67157C3 5.33461 3.26339 5.9705 3.73223 6.43934L4.43934 7.14645C4.6346 7.34171 4.6346 7.65829 4.43934 7.85355L3.43934 8.85355C3.15803 9.13486 3 9.51639 3 9.91421V14H1V15H14V14H12.0001V9.91421C12.0001 9.51639 11.8421 9.13486 11.5608 8.85355L10.5608 7.85355C10.3655 7.65829 10.3655 7.34171 10.5608 7.14645L11.5608 6.14645C11.8421 5.86514 12.0001 5.48361 12.0001 5.08579V1ZM4.24951 5.5H10.793L10.8536 5.43934C10.9474 5.34557 11.0001 5.21839 11.0001 5.08579V1H4V4.67157C4 4.96841 4.08798 5.25617 4.24951 5.5Z"
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
@prop export let ariaLabel = 'hourglass';
-->
