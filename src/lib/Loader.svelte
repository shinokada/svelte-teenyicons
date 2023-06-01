<script lang="ts">
  export let size: string = '15';
  export let role: string = 'img';
  export let color: string = 'black';
  export let variation: 'solid' | 'outline' = 'outline';
  export let ariaLabel = 'loader';
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
      d="M8 1V0.5H7V1H8ZM7 4.5V5H8V4.5H7ZM8 10.5V10H7V10.5H8ZM7 14V14.5H8V14H7ZM4.5 7.99548H5V6.99548H4.5V7.99548ZM1 6.99548H0.5V7.99548H1V6.99548ZM13.9994 8L14.4994 8.00064L14.5006 7.00065L14.0006 7L13.9994 8ZM10.5006 6.99548L10.0006 6.99484L9.99936 7.99484L10.4994 7.99548L10.5006 6.99548ZM7 1V4.5H8V1H7ZM7 10.5V14H8V10.5H7ZM4.5 6.99548H1V7.99548H4.5V6.99548ZM14.0006 7L10.5006 6.99548L10.4994 7.99548L13.9994 8L14.0006 7ZM2.14645 2.85355L5.14645 5.85355L5.85355 5.14645L2.85355 2.14645L2.14645 2.85355ZM12.1464 2.14645L9.14645 5.14645L9.85355 5.85355L12.8536 2.85355L12.1464 2.14645ZM2.85355 12.8536L5.85355 9.85355L5.14645 9.14645L2.14645 12.1464L2.85355 12.8536ZM9.14645 9.85355L12.1464 12.8536L12.8536 12.1464L9.85355 9.14645L9.14645 9.85355Z"
      fill={color}
    />
  {:else}
    <path
      fill-rule="evenodd"
      clip-rule="evenodd"
      d="M8 0.5V5H7V0.5H8ZM5.14645 5.85355L2.14645 2.85355L2.85355 2.14645L5.85355 5.14645L5.14645 5.85355ZM9.14645 5.14645L12.1464 2.14645L12.8536 2.85355L9.85355 5.85355L9.14645 5.14645ZM10.0006 6.99484L14.5006 7.00065L14.4994 8.00064L9.99936 7.99484L10.0006 6.99484ZM0.5 6.99548H5V7.99548H0.5V6.99548ZM5.85355 9.85355L2.85355 12.8536L2.14645 12.1464L5.14645 9.14645L5.85355 9.85355ZM12.1464 12.8536L9.14645 9.85355L9.85355 9.14645L12.8536 12.1464L12.1464 12.8536ZM8 10V14.5H7V10H8Z"
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
