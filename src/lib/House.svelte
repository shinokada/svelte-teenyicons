<script lang="ts">
  export let size: string = "15";
  export let color: string = "black" 
  export let variation: "solid" | "outline" = "outline";
export let ariaLabel="house" </script>

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
    <path d="M0.5 5.5L0.209381 5.09313L0 5.24269V5.5H0.5ZM7.5 0.5L7.79062 0.0931333C7.61677 -0.0310444 7.38323 -0.0310444 7.20938 0.0931333L7.5 0.5ZM14.5 5.5H15V5.24269L14.7906 5.09313L14.5 5.5ZM2.5 8.5V8H2V8.5H2.5ZM6.5 8.5H7V8H6.5V8.5ZM1 15V5.5H0V15H1ZM0.790619 5.90687L7.79062 0.906867L7.20938 0.0931333L0.209381 5.09313L0.790619 5.90687ZM7.20938 0.906867L14.2094 5.90687L14.7906 5.09313L7.79062 0.0931333L7.20938 0.906867ZM14 5.5V15H15V5.5H14ZM3 15V8.5H2V15H3ZM2.5 9H6.5V8H2.5V9ZM6 8.5V15H7V8.5H6ZM5 12H6.5V11H5V12ZM11 8V12H12V8H11ZM13 2V4.5H14V2H13Z" fill="{color}"/> 
  {:else}
    <path fill-rule="evenodd" clip-rule="evenodd" d="M7.79062 0.0931333C7.61677 -0.0310444 7.38323 -0.0310444 7.20938 0.0931333L0.209381 5.09313C0.0779828 5.18699 0 5.33852 0 5.5V14.5C0 14.7761 0.223858 15 0.5 15H2V8H7V15H14.5C14.7761 15 15 14.7761 15 14.5V5.5C15 5.33852 14.922 5.18699 14.7906 5.09313L14 4.52841V2H13V3.81412L7.79062 0.0931333ZM11 12V8H12V12H11Z" fill="{color}"/> <path d="M6 15V12H5V11H6V9H3V15H6Z" fill="{color}"/> 
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