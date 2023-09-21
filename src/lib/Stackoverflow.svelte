<script lang="ts">
  export let size: string = '15';
  export let role: string = 'img';
  export let color: string = 'currentColor';
  export let variation: 'solid' | 'outline' = 'outline';
  export let ariaLabel = 'stackoverflow';
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
      d="M2.5 9V14.5H12.5V9M4 12.5H11M4 10L11 10.7M4.29999 7.5L11 9M5.29999 4.5L11.4 7.6M7 2L12 6.50002M9.5 0.5L13 5.5"
      stroke={color}
    />
  {:else}
    <path
      fill-rule="evenodd"
      clip-rule="evenodd"
      d="M12.5904 5.78672L9.09038 0.786719L9.90962 0.213257L13.4096 5.21326L12.5904 5.78672ZM11.6655 6.87166L6.66552 2.37163L7.33448 1.62834L12.3345 6.12837L11.6655 6.87166ZM11.1735 8.04573L5.07346 4.94573L5.52651 4.05425L11.6265 7.15425L11.1735 8.04573ZM10.8908 9.48791L4.19075 7.98791L4.40922 7.01207L11.1092 8.51207L10.8908 9.48791ZM2 8.99999H3V14H12V8.99999H13V15H2V8.99999ZM10.9502 11.1975L3.95025 10.4975L4.04975 9.50247L11.0498 10.2025L10.9502 11.1975ZM11 13H4V12H11V13Z"
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
@prop export let ariaLabel = 'stackoverflow';
-->
