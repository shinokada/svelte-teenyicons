<script lang="ts">
  export let size: string = "15";
  export let color: string = "black" 
  export let variation: "solid" | "outline" = "outline";
export let ariaLabel="bottom right" </script>

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
    <path d="M13.5 13.5V14C13.7761 14 14 13.7761 14 13.5H13.5ZM13.5 13H8V14H13.5V13ZM14 13.5V8H13V13.5H14ZM13.8535 13.1464L1.85355 1.14645L1.14645 1.85355L13.1464 13.8536L13.8535 13.1464Z" fill="{color}"/> 
  {:else}
    <path fill-rule="evenodd" clip-rule="evenodd" d="M1.85355 1.14645L13 12.2929V8.00001H14V14H8V13H12.2929L1.14645 1.85356L1.85355 1.14645Z" fill="{color}"/> 
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