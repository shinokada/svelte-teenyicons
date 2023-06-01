<script lang="ts">
  export let size: string = '15';
  export let role: string = 'img';
  export let color: string = 'black';
  export let variation: 'solid' | 'outline' = 'outline';
  export let ariaLabel = 'arrow down circle';
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
      d="M5.85355 8.14645L5.5 7.79289L4.79289 8.5L5.14645 8.85355L5.85355 8.14645ZM7.5 10.5L7.14645 10.8536L7.5 11.2071L7.85355 10.8536L7.5 10.5ZM9.85355 8.85355L10.2071 8.5L9.5 7.79289L9.14645 8.14645L9.85355 8.85355ZM0.5 7.5H0H0.5ZM7.5 0.5V0V0.5ZM7.5 14.5V14V14.5ZM14.5 7.5H14H14.5ZM5.14645 8.85355L7.14645 10.8536L7.85355 10.1464L5.85355 8.14645L5.14645 8.85355ZM7.85355 10.8536L9.85355 8.85355L9.14645 8.14645L7.14645 10.1464L7.85355 10.8536ZM8 10.5V4H7V10.5H8ZM1 7.5C1 3.91015 3.91015 1 7.5 1V0C3.35786 -1.78814e-07 1.78814e-07 3.35786 0 7.5H1ZM7.5 14C3.91015 14 1 11.0899 1 7.5H0C-1.78814e-07 11.6421 3.35786 15 7.5 15V14ZM14 7.5C14 11.0899 11.0899 14 7.5 14V15C11.6421 15 15 11.6421 15 7.5H14ZM15 7.5C15 3.35787 11.6421 1.78814e-07 7.5 0V1C11.0899 1 14 3.91015 14 7.5H15Z"
      fill={color}
    />
  {:else}
    <path
      fill-rule="evenodd"
      clip-rule="evenodd"
      d="M7.50005 0C11.6422 1.81058e-07 15 3.35786 15 7.5C15 11.6421 11.6422 15 7.50005 15C3.35791 15 4.55953e-05 11.6421 4.57764e-05 7.5C4.59574e-05 3.35786 3.35791 -1.81058e-07 7.50005 0ZM10.2071 8.49995L7.49997 11.2071L4.79286 8.49995L5.49997 7.79285L7.00005 9.29292V4H8.00005V9.29277L9.49997 7.79285L10.2071 8.49995Z"
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
