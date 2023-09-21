<script lang="ts">
  export let size: string = '15';
  export let role: string = 'img';
  export let color: string = 'currentColor';
  export let variation: 'solid' | 'outline' = 'outline';
  export let ariaLabel = 'align bottom';
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
    <path d="M15 14.5H0M11.5 11.5H8.5V4.5H11.5V11.5ZM6.5 11.5H3.5V0.5H6.5V11.5Z" stroke={color} />
  {:else}
    <path d="M7 0H3V12H7V0Z" fill={color} /> <path d="M12 4H8V12H12V4Z" fill={color} />
    <path d="M15 14H0V15H15V14Z" fill={color} />
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
@prop export let ariaLabel = 'align bottom';
-->
