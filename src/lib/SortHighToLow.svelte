<script lang="ts">
  export let size: string = '15';
  export let role: string = 'img';
  export let color: string = 'currentColor';
  export let variation: 'solid' | 'outline' = 'outline';
  export let ariaLabel = 'sort high to low';
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
      d="M11.5 0.5H12C12 0.223858 11.7761 0 11.5 0V0.5ZM12.5 11.5L12.9743 11.6581L12.5 11.5ZM12.9819 10.0543L12.5076 9.89614L12.9819 10.0543ZM4.5 14.5L4.14645 14.8536C4.24021 14.9473 4.36739 15 4.5 15C4.63261 15 4.75978 14.9473 4.85355 14.8536L4.5 14.5ZM10 1H11.5V0H10V1ZM11 0.5V6.5H12V0.5H11ZM10 7H13V6H10V7ZM11.8617 8H11V9H11.8617V8ZM12.9743 11.6581L13.4563 10.2124L12.5076 9.89614L12.0257 11.3419L12.9743 11.6581ZM11 12H12.5V11H11V12ZM11.9743 14.6581L12.9743 11.6581L12.0257 11.3419L11.0257 14.3419L11.9743 14.6581ZM9 10C9 11.1046 9.89543 12 11 12V11C10.4477 11 10 10.5523 10 10H9ZM11 8C9.89543 8 9 8.89543 9 10H10C10 9.44772 10.4477 9 11 9V8ZM11.8617 9C12.3264 9 12.6545 9.45527 12.5076 9.89614L13.4563 10.2124C13.8191 9.12397 13.0089 8 11.8617 8V9ZM4.85355 14.8536L7.85355 11.8536L7.14645 11.1464L4.14645 14.1464L4.85355 14.8536ZM4.85355 14.1464L1.85355 11.1464L1.14645 11.8536L4.14645 14.8536L4.85355 14.1464ZM4 0V14.5H5V0H4Z"
      fill={color}
    />
  {:else}
    <path
      fill-rule="evenodd"
      clip-rule="evenodd"
      d="M4.00001 13.2929V0H5.00001V13.2929L7.14645 11.1464L7.85356 11.8536L4.85356 14.8536C4.75979 14.9473 4.63262 15 4.50001 15C4.3674 15 4.24022 14.9473 4.14645 14.8536L1.14645 11.8536L1.85356 11.1464L4.00001 13.2929ZM11 1H10V0H11.5C11.7761 0 12 0.223858 12 0.5V6H13V7H10V6H11V1ZM9.00001 10C9.00001 8.89543 9.89544 8 11 8H11.8617C13.009 8 13.8191 9.12397 13.4563 10.2124L11.9743 14.6581L11.0257 14.3419L11.8063 12H11C9.89544 12 9.00001 11.1046 9.00001 10ZM12.1396 11L12.5076 9.89614C12.6545 9.45527 12.3264 9 11.8617 9H11C10.4477 9 10 9.44772 10 10C10 10.5523 10.4477 11 11 11H12.1396Z"
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
@prop export let ariaLabel = 'sort high to low';
-->
