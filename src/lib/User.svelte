<script lang="ts">
  export let size: string = '15';
  export let role: string = 'img';
  export let color: string = 'currentColor';
  export let variation: 'solid' | 'outline' = 'outline';
  export let ariaLabel = 'user';
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
      fill-rule="evenodd"
      clip-rule="evenodd"
      d="M10.5 3.49804C10.5 5.15396 9.157 6.49609 7.5 6.49609C5.843 6.49609 4.5 5.15396 4.5 3.49804C4.5 1.84212 5.843 0.5 7.5 0.5C9.157 0.5 10.5 1.84212 10.5 3.49804Z"
      stroke={color}
      stroke-linecap="square"
    />
    <path
      fill-rule="evenodd"
      clip-rule="evenodd"
      d="M12.5 14.4909H2.5C2.5 13.7808 2.5 13.1053 2.5 12.4936C2.5 10.8368 3.84315 9.49414 5.5 9.49414H9.5C11.1569 9.49414 12.5 10.8368 12.5 12.4936C12.5 13.1053 12.5 13.7808 12.5 14.4909Z"
      stroke={color}
      stroke-linecap="square"
    />
  {:else}
    <path
      d="M7.5 0C5.56717 0 4 1.56567 4 3.49804C4 5.43041 5.56717 6.99609 7.5 6.99609C9.43283 6.99609 11 5.43041 11 3.49804C11 1.56567 9.43283 0 7.5 0Z"
      fill={color}
    />
    <path
      d="M5.5 8.99414C3.56711 8.99414 2 10.5605 2 12.4936V14.9909H13V12.4936C13 10.5605 11.4329 8.99414 9.5 8.99414H5.5Z"
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
@prop export let ariaLabel = 'user';
-->
