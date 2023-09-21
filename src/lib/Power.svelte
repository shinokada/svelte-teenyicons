<script lang="ts">
  export let size: string = '15';
  export let role: string = 'img';
  export let color: string = 'currentColor';
  export let variation: 'solid' | 'outline' = 'outline';
  export let ariaLabel = 'power';
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
      d="M7.50024 8.5V0.5M2.618 2.49866C1.317 3.76883 0.5 5.53376 0.5 7.49548C0.5 11.359 3.635 14.5 7.5 14.5C11.367 14.5 14.5 11.359 14.5 7.49548C14.5 5.53676 13.693 3.76883 12.395 2.49866"
      stroke={color}
      stroke-linecap="square"
    />
  {:else}
    <path
      fill-rule="evenodd"
      clip-rule="evenodd"
      d="M8.00024 0V9H7.00024V0H8.00024ZM12.3873 1.79159L12.7447 2.14129C14.1345 3.50125 15 5.39628 15 7.49548C15 11.6345 11.6437 15 7.5 15C3.35837 15 0 11.6346 0 7.49548C0 5.39135 0.877013 3.49961 2.26871 2.14089L2.62648 1.7916L3.32506 2.50714L2.96729 2.85642C1.75699 4.03804 1 5.67618 1 7.49548C1 11.0833 3.91163 14 7.5 14C11.0903 14 14 11.0834 14 7.49548C14 5.67725 13.2515 4.03641 12.0453 2.85602L11.6879 2.50632L12.3873 1.79159Z"
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
@prop export let ariaLabel = 'power';
-->
