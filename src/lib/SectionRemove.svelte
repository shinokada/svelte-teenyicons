<script lang="ts">
  export let size: string = '15';
  export let color: string = 'black';
  export let variation: 'solid' | 'outline' = 'outline';
  export let ariaLabel = 'section remove';
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
      d="M4 0.5H1.5C0.947715 0.5 0.5 0.947715 0.5 1.5V4M6 0.5H9M11 0.5H13.5C14.0523 0.5 14.5 0.947715 14.5 1.5V4M0.5 6V9M14.5 6V9M0.5 11V13.5C0.5 14.0523 0.947715 14.5 1.5 14.5H4M14.5 11V13.5C14.5 14.0523 14.0523 14.5 13.5 14.5H11M4 7.5H11M6 14.5H9"
      stroke={color}
    />
  {:else}
    <path
      fill-rule="evenodd"
      clip-rule="evenodd"
      d="M0 1.5C0 0.671573 0.671573 0 1.5 0H4V1H1.5C1.22386 1 1 1.22386 1 1.5V4H0V1.5ZM9 1H6V0H9V1ZM13.5 1H11V0H13.5C14.3284 0 15 0.671573 15 1.5V4H14V1.5C14 1.22386 13.7761 1 13.5 1ZM0 9V6H1V9H0ZM14 9V6H15V9H14ZM11 8H4V7H11V8ZM0 13.5V11H1V13.5C1 13.7761 1.22386 14 1.5 14H4V15H1.5C0.671573 15 0 14.3284 0 13.5ZM14 13.5V11H15V13.5C15 14.3284 14.3284 15 13.5 15H11V14H13.5C13.7761 14 14 13.7761 14 13.5ZM9 15H6V14H9V15Z"
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
