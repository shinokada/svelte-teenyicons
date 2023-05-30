<script lang="ts">
  export let size: string = '15';
  export let color: string = 'black';
  export let variation: 'solid' | 'outline' = 'outline';
  export let ariaLabel = 'computer';
</script>

<svg
  xmlns="http://www.w3.org/2000/svg"
  width={size}
  height={size}
  fill="none"
  class={$$props.class}
  {...$$restProps}
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
      d="M9.5 14.5H13.5C14.0523 14.5 14.5 14.0523 14.5 13.5V1.5C14.5 0.947715 14.0523 0.5 13.5 0.5H9.5C8.94772 0.5 8.5 0.947716 8.5 1.5V13.5C8.5 14.0523 8.94772 14.5 9.5 14.5ZM9.5 14.5H4M6.5 11.5V14.5M8.5 5.5H14.5M10 11.5H13M1.5 3.5H8.5V11.5H1.5C0.947715 11.5 0.5 11.0523 0.5 10.5V4.5C0.5 3.94772 0.947715 3.5 1.5 3.5Z"
      stroke={color}
    />
  {:else}
    <path d="M10 12H13V11H10V12Z" fill={color} />
    <path
      fill-rule="evenodd"
      clip-rule="evenodd"
      d="M9.5 0C8.67157 0 8 0.671573 8 1.5V3H1.5C0.671573 3 0 3.67157 0 4.5V10.5C0 11.3284 0.671573 12 1.5 12H6V14H4V15H13.5C14.3284 15 15 14.3284 15 13.5V1.5C15 0.671573 14.3284 0 13.5 0H9.5ZM8.08535 14H7V12H8V13.5C8 13.6753 8.03008 13.8436 8.08535 14ZM9.5 14H13.5C13.7761 14 14 13.7761 14 13.5V6H9V13.5C9 13.7761 9.22386 14 9.5 14ZM9 5H14V1.5C14 1.22386 13.7761 1 13.5 1H9.5C9.22386 1 9 1.22386 9 1.5V5Z"
      fill={color}
    />
  {/if}
</svg>

<!--
  @component
  [Go to Document](https://svelte-teenyicons.codewithshin.com/)

  ## Props
  @prop size: string = "15";
  @prop color: string = "black" 
  @prop variation: "solid" | "outline" = "outline";
-->
