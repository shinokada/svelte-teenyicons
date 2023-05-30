<script lang="ts">
  export let size: string = "15";
  export let color: string = "black" 
  export let variation: "solid" | "outline" = "outline";
export let ariaLabel="bank" </script>

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
    <path d="M7.5 0.5L7.72361 0.0527866C7.58284 -0.0175955 7.41716 -0.0175955 7.27639 0.0527866L7.5 0.5ZM0 15H15V14H0V15ZM7.27639 0.0527866L1.27639 3.05279L1.72361 3.94722L7.72361 0.947213L7.27639 0.0527866ZM0 6.00001H15V5.00001H0V6.00001ZM13.7236 3.05279L7.72361 0.0527866L7.27639 0.947213L13.2764 3.94722L13.7236 3.05279ZM5 8.00001V12H6V8.00001H5ZM9 8.00001V12H10V8.00001H9ZM1 5.50001V14.5H2V5.50001H1ZM13 5.50001V14.5H14V5.50001H13Z" fill="{color}"/> 
  {:else}
    <path d="M7.72361 0.0527864C7.58284 -0.0175955 7.41716 -0.0175955 7.27639 0.0527864L1.27639 3.05279L1.72361 3.94721L7.5 1.05902L13.2764 3.94721L13.7236 3.05279L7.72361 0.0527864Z" fill="{color}"/> <path fill-rule="evenodd" clip-rule="evenodd" d="M14 6H15V5H0V6H1V14H0V15H15V14H14V6ZM5 12V8H6V12H5ZM9 12V8H10V12H9Z" fill="{color}"/> 
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