<script lang="ts">
  export let size: string = '15';
  export let color: string = 'black';
  export let variation: 'solid' | 'outline' = 'outline';
  export let ariaLabel = 'edit circle';
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
      d="M4.5 8.5L4.14645 8.14645L4 8.29289V8.5H4.5ZM8.5 4.5L8.85355 4.14645C8.65829 3.95118 8.34171 3.95118 8.14645 4.14645L8.5 4.5ZM10.5 6.5L10.8536 6.85355C11.0488 6.65829 11.0488 6.34171 10.8536 6.14645L10.5 6.5ZM6.5 10.5V11H6.70711L6.85355 10.8536L6.5 10.5ZM4.5 10.5H4C4 10.7761 4.22386 11 4.5 11V10.5ZM7.5 14C3.91015 14 1 11.0899 1 7.5H0C0 11.6421 3.35786 15 7.5 15V14ZM14 7.5C14 11.0899 11.0899 14 7.5 14V15C11.6421 15 15 11.6421 15 7.5H14ZM7.5 1C11.0899 1 14 3.91015 14 7.5H15C15 3.35786 11.6421 0 7.5 0V1ZM7.5 0C3.35786 0 0 3.35786 0 7.5H1C1 3.91015 3.91015 1 7.5 1V0ZM4.85355 8.85355L8.85355 4.85355L8.14645 4.14645L4.14645 8.14645L4.85355 8.85355ZM8.14645 4.85355L10.1464 6.85355L10.8536 6.14645L8.85355 4.14645L8.14645 4.85355ZM10.1464 6.14645L6.14645 10.1464L6.85355 10.8536L10.8536 6.85355L10.1464 6.14645ZM6.5 10H4.5V11H6.5V10ZM5 10.5V8.5H4V10.5H5Z"
      fill={color}
    />
  {:else}
    <path
      fill-rule="evenodd"
      clip-rule="evenodd"
      d="M0 7.5C0 3.35786 3.35786 0 7.5 0C11.6421 0 15 3.35786 15 7.5C15 11.6421 11.6421 15 7.5 15C3.35786 15 0 11.6421 0 7.5ZM8.14645 4.14645C8.34171 3.95118 8.65829 3.95118 8.85355 4.14645L10.8536 6.14645C11.0488 6.34171 11.0488 6.65829 10.8536 6.85355L6.70711 11H4.5C4.22386 11 4 10.7761 4 10.5V8.29289L8.14645 4.14645Z"
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
-->
