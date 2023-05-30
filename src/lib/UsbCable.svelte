<script lang="ts">
  export let size: string = "15";
  export let color: string = "black" 
  export let variation: "solid" | "outline" = "outline";
export let ariaLabel="usb cable" </script>

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
    <path d="M4.5 5.5H10.5M4.5 5.5C3.94772 5.5 3.5 5.94772 3.5 6.5V10.5C3.5 11.0523 3.94772 11.5 4.5 11.5H10.5C11.0523 11.5 11.5 11.0523 11.5 10.5V6.5C11.5 5.94772 11.0523 5.5 10.5 5.5M4.5 5.5V0.5H10.5V5.5M6.5 2V4M8.5 2V4M5.5 11.5V13.5H9.5V11.5M6.5 13.5V15M8.5 13.5V15" stroke="{color}"/> 
  {:else}
    <path fill-rule="evenodd" clip-rule="evenodd" d="M11 0H4V6H11V0ZM6 4V2H7V4H6ZM8 4V2H9V4H8Z" fill="{color}"/> <path d="M12 7H3V10.5C3 11.3284 3.67157 12 4.5 12H5V14H6V15H7V14H8V15H9V14H10V12H10.5C11.3284 12 12 11.3284 12 10.5V7Z" fill="{color}"/> 
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