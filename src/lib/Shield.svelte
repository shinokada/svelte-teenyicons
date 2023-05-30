<script lang="ts">
  export let size: string = '15';
  export let color: string = 'black';
  export let variation: 'solid' | 'outline' = 'outline';
  export let ariaLabel = 'shield';
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
      d="M0.5 4.5L7.5 0.5L14.5 4.5V5.21989C14.5 9.52908 11.6434 13.3162 7.5 14.5C3.35661 13.3162 0.5 9.52908 0.5 5.21989V4.5Z"
      stroke={color}
      stroke-linecap="round"
      stroke-linejoin="round"
    />
  {:else}
    <path
      d="M7.74807 0.0658784C7.59435 -0.0219595 7.40565 -0.0219595 7.25193 0.0658784L0.251931 4.06588C0.096143 4.1549 0 4.32057 0 4.5V5.21989C0 9.75232 3.0046 13.7356 7.36264 14.9808C7.45242 15.0064 7.54758 15.0064 7.63736 14.9808C11.9954 13.7356 15 9.75232 15 5.21989V4.5C15 4.32057 14.9039 4.1549 14.7481 4.06588L7.74807 0.0658784Z"
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
