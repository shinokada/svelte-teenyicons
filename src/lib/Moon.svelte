<script lang="ts">
  export let size: string = '15';
  export let color: string = 'black';
  export let variation: 'solid' | 'outline' = 'outline';
  export let ariaLabel = 'moon';
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
      d="M1.66077 11.3619C2.09296 11.4524 2.54093 11.5 3.00002 11.5C6.58987 11.5 9.50002 8.58987 9.50002 5.00002C9.50002 3.25482 8.81224 1.67027 7.69295 0.502625C11.4697 0.604839 14.5 3.69855 14.5 7.50002C14.5 11.366 11.366 14.5 7.49999 14.5C5.06138 14.5 2.91401 13.253 1.66077 11.3619Z"
      stroke={color}
      stroke-linejoin="round"
    />
  {:else}
    <path
      d="M7.7066 0.00274765C7.50391 -0.0027381 7.31797 0.114737 7.23588 0.300147C7.15379 0.485558 7.19181 0.702186 7.33213 0.848565C8.36577 1.92686 9.00015 3.3888 9.00015 4.99996C9.00015 8.31366 6.31385 11 3.00015 11C2.5757 11 2.16207 10.956 1.76339 10.8725C1.56489 10.8309 1.36094 10.9133 1.2471 11.0812C1.13325 11.249 1.13207 11.469 1.2441 11.638C2.58602 13.663 4.88682 15 7.50012 15C11.6423 15 15.0001 11.6421 15.0001 7.49996C15.0001 3.42688 11.7534 0.112271 7.7066 0.00274765Z"
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
