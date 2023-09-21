<script lang="ts">
  export let size: string = '15';
  export let role: string = 'img';
  export let color: string = 'currentColor';
  export let variation: 'solid' | 'outline' = 'outline';
  export let ariaLabel = 'folder x';
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
      d="M5.5 6.5L9.5 10.5M5.5 10.5L9.5 6.5M0.5 2.5V12.5C0.5 13.0523 0.947715 13.5 1.5 13.5H13.5C14.0523 13.5 14.5 13.0523 14.5 12.5V4.5C14.5 3.94772 14.0523 3.5 13.5 3.5H7.5L5.5 1.5H1.5C0.947715 1.5 0.5 1.94772 0.5 2.5Z"
      stroke={color}
    />
  {:else}
    <path
      fill-rule="evenodd"
      clip-rule="evenodd"
      d="M0 2.5C0 1.67157 0.671573 1 1.5 1H5.70711L7.70711 3H13.5C14.3284 3 15 3.67157 15 4.5V12.5C15 13.3284 14.3284 14 13.5 14H1.5C0.671573 14 0 13.3284 0 12.5V2.5ZM9.14648 10.8536L7.50004 9.20714L5.85359 10.8536L5.14648 10.1465L6.79293 8.50004L5.14648 6.85359L5.85359 6.14648L7.50004 7.79293L9.14648 6.14648L9.85359 6.85359L8.20714 8.50004L9.85359 10.1465L9.14648 10.8536Z"
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
@prop export let ariaLabel = 'folder x';
-->
