<script lang="ts">
  export let size: string = '15';
  export let color: string = 'black';
  export let variation: 'solid' | 'outline' = 'outline';
  export let ariaLabel = 'caret vertical';
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
      d="M7.5 13L7.16782 13.3737L7.5 13.669L7.83218 13.3737L7.5 13ZM7.5 2L7.84002 1.63341L7.50715 1.32467L7.16782 1.6263L7.5 2ZM7.83218 13.3737L12.3322 9.3737L11.6678 8.6263L7.16782 12.6263L7.83218 13.3737ZM7.83218 12.6263L3.33218 8.6263L2.66782 9.3737L7.16782 13.3737L7.83218 12.6263ZM7.16782 1.6263L2.66782 5.6263L3.33218 6.3737L7.83218 2.3737L7.16782 1.6263ZM7.15998 2.36659L11.4725 6.36659L12.1525 5.63341L7.84002 1.63341L7.15998 2.36659Z"
      fill={color}
    />
  {:else}
    <path d="M7.49991 1.33563L2.16919 6.00002H12.8306L7.49991 1.33563Z" fill={color} />
    <path d="M7.50009 13.6644L12.8308 9.00002H2.16936L7.50009 13.6644Z" fill={color} />
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
