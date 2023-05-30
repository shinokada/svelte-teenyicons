<script lang="ts">
  export let size: string = '15';
  export let color: string = 'black';
  export let variation: 'solid' | 'outline' = 'outline';
  export let ariaLabel = 'double caret left';
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
    <path d="M8 1L1 7.5L8 14M13.5 1L6.5 7.5L13.5 14" stroke={color} stroke-linecap="square" />
  {:else}
    <path
      fill-rule="evenodd"
      clip-rule="evenodd"
      d="M8.70665 1.02619L1.73483 7.50002L8.70665 13.9738L8.02619 14.7066L0.265217 7.50002L8.0262 0.293396L8.70665 1.02619ZM14.2066 1.02619L7.23483 7.50002L14.2066 13.9738L13.5262 14.7066L5.76522 7.50002L13.5262 0.293396L14.2066 1.02619Z"
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
  @prop ariaLabel = 'icon file name';
  ## Event
  - on:click 
  - on:mouseenter 
  - on:mouseleave 
  - on:mouseover 
  - on:mouseout 
  - on:blur 
  - on:focus 
-->
