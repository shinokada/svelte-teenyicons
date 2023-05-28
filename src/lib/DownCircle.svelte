<script lang="ts">
  export let size: string = "15";
  export let color: string = "black" 
  export let variation: "solid" | "outline" = "outline";
export let ariaLabel="down circle" </script>

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
    <path d="M4.85355 6.14645L4.5 5.79289L3.79289 6.5L4.14645 6.85355L4.85355 6.14645ZM7.5 9.5L7.14645 9.85355L7.5 10.2071L7.85355 9.85355L7.5 9.5ZM10.8536 6.85355L11.2071 6.5L10.5 5.79289L10.1464 6.14645L10.8536 6.85355ZM4.14645 6.85355L7.14645 9.85355L7.85355 9.14645L4.85355 6.14645L4.14645 6.85355ZM7.85355 9.85355L10.8536 6.85355L10.1464 6.14645L7.14645 9.14645L7.85355 9.85355ZM14 7.5C14 11.0899 11.0898 14 7.5 14V15C11.6421 15 15 11.6421 15 7.5H14ZM7.5 1C11.0899 1 14 3.91015 14 7.5H15C15 3.35787 11.6421 5.36442e-07 7.5 0V1ZM1 7.5C1 3.91015 3.91015 1 7.5 1V0C3.35787 -5.36442e-07 5.36442e-07 3.35786 0 7.5H1ZM0 7.5C-5.36442e-07 11.6421 3.35786 15 7.5 15V14C3.91015 14 1 11.0898 1 7.5H0Z" fill="{color}"/> 
  {:else}
    <path fill-rule="evenodd" clip-rule="evenodd" d="M7.5 15C3.35786 15 0 11.6421 0 7.5C0 3.35786 3.35787 0 7.5 0C11.6421 0 15 3.35787 15 7.5C15 11.6421 11.6421 15 7.5 15ZM11.7069 6L7.49983 10.2071L3.29272 6H11.7069Z" fill="{color}"/> 
  {/if}
</svg>
