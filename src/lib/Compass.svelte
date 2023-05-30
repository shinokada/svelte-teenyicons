<script lang="ts">
  export let size: string = '15';
  export let color: string = 'black';
  export let variation: 'solid' | 'outline' = 'outline';
  export let ariaLabel = 'compass';
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
      d="M4.5 10.5L4.05279 10.2764C3.95654 10.4689 3.99427 10.7014 4.14645 10.8536C4.29863 11.0057 4.53111 11.0435 4.72361 10.9472L4.5 10.5ZM6.5 6.5L6.27639 6.05279C6.17963 6.10117 6.10117 6.17963 6.05279 6.27639L6.5 6.5ZM10.5 4.5L10.9472 4.72361C11.0435 4.53111 11.0057 4.29863 10.8536 4.14645C10.7014 3.99427 10.4689 3.95654 10.2764 4.05279L10.5 4.5ZM8.5 8.5L8.72361 8.94721C8.82037 8.89883 8.89883 8.82037 8.94721 8.72361L8.5 8.5ZM7.5 14C3.91015 14 1 11.0899 1 7.5H0C0 11.6421 3.35786 15 7.5 15V14ZM14 7.5C14 11.0899 11.0899 14 7.5 14V15C11.6421 15 15 11.6421 15 7.5H14ZM7.5 1C11.0899 1 14 3.91015 14 7.5H15C15 3.35786 11.6421 0 7.5 0V1ZM7.5 0C3.35786 0 0 3.35786 0 7.5H1C1 3.91015 3.91015 1 7.5 1V0ZM4.94721 10.7236L6.94721 6.72361L6.05279 6.27639L4.05279 10.2764L4.94721 10.7236ZM6.72361 6.94721L10.7236 4.94721L10.2764 4.05279L6.27639 6.05279L6.72361 6.94721ZM10.0528 4.27639L8.05279 8.27639L8.94721 8.72361L10.9472 4.72361L10.0528 4.27639ZM8.27639 8.05279L4.27639 10.0528L4.72361 10.9472L8.72361 8.94721L8.27639 8.05279Z"
      fill={color}
    />
  {:else}
    <path
      d="M5.61805 9.38198L6.87269 6.87269L9.38198 5.61805L8.12734 8.12734L5.61805 9.38198Z"
      fill={color}
    />
    <path
      fill-rule="evenodd"
      clip-rule="evenodd"
      d="M0 7.5C0 3.35786 3.35786 0 7.5 0C11.6421 0 15 3.35786 15 7.5C15 11.6421 11.6421 15 7.5 15C3.35786 15 0 11.6421 0 7.5ZM10.9472 4.72362C11.0435 4.53113 11.0057 4.29864 10.8536 4.14646C10.7014 3.99428 10.4689 3.95655 10.2764 4.0528L6.27641 6.0528C6.17964 6.10118 6.10118 6.17964 6.0528 6.27641L4.0528 10.2764C3.95655 10.4689 3.99428 10.7014 4.14646 10.8536C4.29864 11.0057 4.53113 11.0435 4.72362 10.9472L8.72362 8.94723C8.82038 8.89885 8.89885 8.82038 8.94723 8.72362L10.9472 4.72362Z"
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
