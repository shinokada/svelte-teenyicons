<script lang="ts">
  export let size: string = '15';
  export let role: string = 'img';
  export let color: string = 'currentColor';
  export let variation: 'solid' | 'outline' = 'outline';
  export let ariaLabel = 'audio document';
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
      d="M13.5 3.5H14V3.29289L13.8536 3.14645L13.5 3.5ZM10.5 0.5L10.8536 0.146447L10.7071 0H10.5V0.5ZM7.5 4.5L7.9 4.2C7.77087 4.02783 7.54606 3.9576 7.34189 4.02566C7.13771 4.09372 7 4.28478 7 4.5H7.5ZM7.8 4.9L8.2 4.6L7.8 4.9ZM12.5 14H2.5V15H12.5V14ZM2 13.5V1.5H1V13.5H2ZM13 3.5V13.5H14V3.5H13ZM2.5 1H10.5V0H2.5V1ZM10.1464 0.853553L13.1464 3.85355L13.8536 3.14645L10.8536 0.146447L10.1464 0.853553ZM2.5 14C2.22386 14 2 13.7761 2 13.5H1C1 14.3284 1.67157 15 2.5 15V14ZM12.5 15C13.3284 15 14 14.3284 14 13.5H13C13 13.7761 12.7761 14 12.5 14V15ZM2 1.5C2 1.22386 2.22386 1 2.5 1V0C1.67157 0 1 0.671574 1 1.5H2ZM6 11C5.44772 11 5 10.5523 5 10H4C4 11.1046 4.89543 12 6 12V11ZM7 10C7 10.5523 6.55228 11 6 11V12C7.10457 12 8 11.1046 8 10H7ZM6 9C6.55228 9 7 9.44772 7 10H8C8 8.89543 7.10457 8 6 8V9ZM6 8C4.89543 8 4 8.89543 4 10H5C5 9.44772 5.44772 9 6 9V8ZM7 6.5V10H8V6.5H7ZM8 7V4.5H7V7H8ZM7.1 4.8L7.4 5.2L8.2 4.6L7.9 4.2L7.1 4.8ZM7.4 5.2C8.24984 6.33313 9.58359 7 11 7V6C9.89835 6 8.86099 5.48132 8.2 4.6L7.4 5.2Z"
      fill={color}
    />
  {:else}
    <path
      d="M7 10C7 9.44771 6.55228 9 6 9C5.44772 9 5 9.44771 5 10C5 10.5523 5.44772 11 6 11C6.55228 11 7 10.5523 7 10Z"
      fill={color}
    />
    <path
      fill-rule="evenodd"
      clip-rule="evenodd"
      d="M1 1.5C1 0.671573 1.67157 0 2.5 0H10.7071L14 3.29289V13.5C14 14.3284 13.3284 15 12.5 15H2.5C1.67157 15 1 14.3284 1 13.5V1.5ZM7.34189 4.02569C7.54606 3.95763 7.77087 4.02786 7.9 4.20003L8.2 4.60003C8.86099 5.48135 9.89835 6.00003 11 6.00003V7.00003C9.88299 7.00003 8.8174 6.58529 8 5.8542V10C8 11.1046 7.10457 12 6 12C4.89543 12 4 11.1046 4 10C4 8.89543 4.89543 8 6 8C6.36429 8 6.70583 8.09739 7 8.26756V4.50003C7 4.28482 7.13772 4.09375 7.34189 4.02569Z"
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
@prop export let ariaLabel = 'audio document';
-->
