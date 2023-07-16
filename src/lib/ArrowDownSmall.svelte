<script lang="ts">
  export let size: string = "15";
  export let role: string = "img";
  export let color: string = "currentColor" 
  export let variation: "solid" | "outline" = "outline";
export let ariaLabel="arrow down small" </script>

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
    <path d="M9.85355 8.85355L10.2071 8.5L9.5 7.79289L9.14645 8.14645L9.85355 8.85355ZM7.5 10.5L7.14645 10.8536L7.5 11.2071L7.85355 10.8536L7.5 10.5ZM5.85355 8.14645L5.5 7.79289L4.79289 8.5L5.14645 8.85355L5.85355 8.14645ZM9.14645 8.14645L7.14645 10.1464L7.85355 10.8536L9.85355 8.85355L9.14645 8.14645ZM7.85355 10.1464L5.85355 8.14645L5.14645 8.85355L7.14645 10.8536L7.85355 10.1464ZM8 10.5L8 4L7 4L7 10.5H8Z" fill="{color}"/> 
  {:else}
    <path fill-rule="evenodd" clip-rule="evenodd" d="M8.00001 4L8.00001 9.29289L9.50001 7.79289L10.2071 8.5L7.50001 11.2071L4.79291 8.5L5.50001 7.79289L7.00001 9.29289L7.00001 4H8.00001Z" fill="{color}"/> 
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