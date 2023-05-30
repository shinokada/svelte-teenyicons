<script lang="ts">
  export let size: string = '15';
  export let color: string = 'black';
  export let variation: 'solid' | 'outline' = 'outline';
  export let ariaLabel = 'brush';
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
      d="M13.5 7.5V2.5C13.5 1.39543 12.6046 0.5 11.5 0.5H3.5C2.39543 0.5 1.5 1.39543 1.5 2.5V7.5M13.5 7.5H1.5M13.5 7.5V9.5C13.5 10.6046 12.6046 11.5 11.5 11.5H8.5V13.5C8.5 14.0523 8.05228 14.5 7.5 14.5C6.94772 14.5 6.5 14.0523 6.5 13.5V11.5H3.5C2.39543 11.5 1.5 10.6046 1.5 9.5V7.5M5.5 0.5V5M7.5 0.5V3"
      stroke={color}
    />
  {:else}
    <path
      fill-rule="evenodd"
      clip-rule="evenodd"
      d="M1 2.5C1 1.11929 2.11929 0 3.5 0H5V5H6V0H7V3H8V0H11.5C12.8807 0 14 1.11929 14 2.5V9.5C14 10.8807 12.8807 12 11.5 12H9V13.5C9 14.3284 8.32843 15 7.5 15C6.67157 15 6 14.3284 6 13.5V12H3.5C2.11929 12 1 10.8807 1 9.5V2.5ZM2 8V9.5C2 10.3284 2.67157 11 3.5 11H7V13.5C7 13.7761 7.22386 14 7.5 14C7.77614 14 8 13.7761 8 13.5V11H11.5C12.3284 11 13 10.3284 13 9.5V8H2Z"
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
