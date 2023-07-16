<script lang="ts">
  export let size: string = '15';
  export let role: string = 'img';
  export let color: string = 'currentColor';
  export let variation: 'solid' | 'outline' = 'outline';
  export let ariaLabel = 'clockwise';
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
      d="M14 8.49475V7.99475H13V8.49475H14ZM7.5 2.99866H8V1.99866H7.5V2.99866ZM8.5 2.49866L8.85345 2.85232L9.20733 2.49865L8.85343 2.14499L8.5 2.49866ZM13 8.49475C13 11.5291 10.5372 13.9908 7.5 13.9908V14.9908C11.0888 14.9908 14 12.082 14 8.49475H13ZM7.5 13.9908C4.46284 13.9908 2 11.5291 2 8.49475H1C1 12.082 3.91116 14.9908 7.5 14.9908V13.9908ZM2 8.49475C2 5.46036 4.46284 2.99866 7.5 2.99866V1.99866C3.91116 1.99866 1 4.90746 1 8.49475H2ZM6.14657 0.853672L8.14657 2.85233L8.85343 2.14499L6.85343 0.146328L6.14657 0.853672ZM8.14655 2.145L6.14655 4.14378L6.85345 4.8511L8.85345 2.85232L8.14655 2.145Z"
      fill={color}
    />
  {:else}
    <path
      fill-rule="evenodd"
      clip-rule="evenodd"
      d="M7.29548 2.00182L6.14657 0.853676L6.85343 0.146332L9.20733 2.49865L6.85345 4.8511L6.14655 4.14378L7.28837 3.00266C4.34925 3.11385 2 5.53116 2 8.49475C2 11.5291 4.46284 13.9908 7.5 13.9908C10.5372 13.9908 13 11.5291 13 8.49475V7.99475H14V8.49475C14 12.082 11.0888 14.9908 7.5 14.9908C3.91116 14.9908 1 12.082 1 8.49475C1 4.97586 3.80121 2.10983 7.29548 2.00182Z"
      fill={color}
    />
  {/if}
</svg>

<!--
  @component
  [Go to Document](https://svelte-teenyicons.codewithshin.com/)

  ## Props
  @prop size: string = "15";
  @prop role: string = "icon file name";
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
