<script lang="ts">
  export let size: string = '15';
  export let color: string = 'black';
  export let variation: 'solid' | 'outline' = 'outline';
  export let ariaLabel = 'bracket';
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
      d="M0 7.5H2M15 7.5H13M5 14.5H3.5C2.39543 14.5 1.5 13.6046 1.5 12.5V2.5C1.5 1.39543 2.39543 0.5 3.5 0.5H5M10 14.5H11.5C12.6046 14.5 13.5 13.6046 13.5 12.5V2.5C13.5 1.39543 12.6046 0.5 11.5 0.5H10"
      stroke={color}
    />
  {:else}
    <path
      fill-rule="evenodd"
      clip-rule="evenodd"
      d="M3.5 1C2.67157 1 2 1.67157 2 2.5V12.5C2 13.3284 2.67157 14 3.5 14H5V15H3.5C2.11929 15 1 13.8807 1 12.5V8H0V7H1V2.5C1 1.11929 2.11929 0 3.5 0H5V1H3.5ZM10 0H11.5C12.8807 0 14 1.11929 14 2.5V7H15V8H14V12.5C14 13.8807 12.8807 15 11.5 15H10V14H11.5C12.3284 14 13 13.3284 13 12.5V2.5C13 1.67157 12.3284 1 11.5 1H10V0Z"
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
