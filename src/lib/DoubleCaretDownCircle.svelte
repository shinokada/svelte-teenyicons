<script lang="ts">
  export let size: string = '15';
  export let role: string = 'img';
  export let color: string = 'currentColor';
  export let variation: 'solid' | 'outline' = 'outline';
  export let ariaLabel = 'double caret down circle';
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
      d="M9.85355 8.85355L10.2071 8.5L9.5 7.79289L9.14645 8.14645L9.85355 8.85355ZM7.5 10.5L7.14645 10.8536L7.5 11.2071L7.85355 10.8536L7.5 10.5ZM5.85355 8.14645L5.5 7.79289L4.79289 8.5L5.14645 8.85355L5.85355 8.14645ZM9.85355 5.85355L10.2071 5.5L9.5 4.79289L9.14645 5.14645L9.85355 5.85355ZM7.5 7.5L7.14645 7.85355L7.5 8.20711L7.85355 7.85355L7.5 7.5ZM5.85355 5.14645L5.5 4.79289L4.79289 5.5L5.14645 5.85355L5.85355 5.14645ZM14.5 7.5H14H14.5ZM7.5 0.5V1V0.5ZM7.5 14.5V15V14.5ZM0.5 7.5H0H0.5ZM9.14645 8.14645L7.14645 10.1464L7.85355 10.8536L9.85355 8.85355L9.14645 8.14645ZM7.85355 10.1464L5.85355 8.14645L5.14645 8.85355L7.14645 10.8536L7.85355 10.1464ZM9.14645 5.14645L7.14645 7.14645L7.85355 7.85355L9.85355 5.85355L9.14645 5.14645ZM7.85355 7.14645L5.85355 5.14645L5.14645 5.85355L7.14645 7.85355L7.85355 7.14645ZM15 7.5C15 3.35787 11.6421 1.78814e-07 7.5 0V1C11.0899 1 14 3.91015 14 7.5H15ZM7.5 15C11.6421 15 15 11.6421 15 7.5H14C14 11.0899 11.0899 14 7.5 14V15ZM0 7.5C-1.78814e-07 11.6421 3.35786 15 7.5 15V14C3.91015 14 1 11.0899 1 7.5H0ZM1 7.5C1 3.91015 3.91015 1 7.5 1V0C3.35787 -1.78814e-07 1.78814e-07 3.35786 0 7.5H1Z"
      fill={color}
    />
  {:else}
    <path
      fill-rule="evenodd"
      clip-rule="evenodd"
      d="M7.50006 0C3.35793 -1.81058e-07 6.12162e-05 3.35786 6.10352e-05 7.5C6.08541e-05 11.6421 3.35792 15 7.50006 15C11.6422 15 15.0001 11.6421 15.0001 7.5C15.0001 3.35786 11.6422 1.81058e-07 7.50006 0ZM4.79303 5.49995L7.50014 8.20706L10.2072 5.49995L9.50014 4.79285L7.50014 6.79285L5.50014 4.79285L4.79303 5.49995ZM4.79303 8.49995L7.50014 11.2071L10.2072 8.49995L9.50014 7.79285L7.50014 9.79285L5.50014 7.79285L4.79303 8.49995Z"
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
@prop export let ariaLabel = 'double caret down circle';
-->
