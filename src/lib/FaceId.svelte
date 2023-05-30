<script lang="ts">
  export let size: string = "15";
  export let color: string = "black" 
  export let variation: "solid" | "outline" = "outline";
export let ariaLabel="face id" </script>

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
    <path d="M4 6H5V5H4V6ZM10 6H11V5H10V6ZM10.1 8.7C8.8 10.4333 6.2 10.4333 4.9 8.7L4.1 9.3C5.8 11.5667 9.2 11.5667 10.9 9.3L10.1 8.7ZM1 5V2.5H0V5H1ZM2.5 1H5V0H2.5V1ZM1 2.5C1 1.67157 1.67157 1 2.5 1V0C1.11929 0 0 1.11929 0 2.5H1ZM0 10V12.5H1V10H0ZM2.5 15H5V14H2.5V15ZM0 12.5C0 13.8807 1.11929 15 2.5 15V14C1.67157 14 1 13.3284 1 12.5H0ZM10 1H12.5V0H10V1ZM14 2.5V5H15V2.5H14ZM12.5 1C13.3284 1 14 1.67157 14 2.5H15C15 1.11929 13.8807 0 12.5 0V1ZM10 15H12.5V14H10V15ZM15 12.5V10H14V12.5H15ZM12.5 15C13.8807 15 15 13.8807 15 12.5H14C14 13.3284 13.3284 14 12.5 14V15Z" fill="{color}"/> 
  {:else}
    <path fill-rule="evenodd" clip-rule="evenodd" d="M2.5 1C1.67157 1 1 1.67157 1 2.5V5H0V2.5C0 1.11929 1.11929 0 2.5 0H5V1H2.5ZM12.5 1H10V0H12.5C13.8807 0 15 1.11929 15 2.5V5H14V2.5C14 1.67157 13.3284 1 12.5 1ZM5 6H4V5H5V6ZM11 6H10V5H11V6ZM4.9 8.7C6.2 10.4333 8.8 10.4333 10.1 8.7L10.9 9.3C9.2 11.5667 5.8 11.5667 4.1 9.3L4.9 8.7ZM0 12.5V10H1V12.5C1 13.3284 1.67157 14 2.5 14H5V15H2.5C1.11929 15 0 13.8807 0 12.5ZM15 10V12.5C15 13.8807 13.8807 15 12.5 15H10V14H12.5C13.3284 14 14 13.3284 14 12.5V10H15Z" fill="{color}"/> 
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