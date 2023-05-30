<script lang="ts">
  export let size: string = "15";
  export let color: string = "black" 
  export let variation: "solid" | "outline" = "outline";
export let ariaLabel="superscript" </script>

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
    <path d="M12.5 3.5L12.1464 3.14645C12.0034 3.28945 11.9607 3.5045 12.0381 3.69134C12.1155 3.87818 12.2978 4 12.5 4V3.5ZM14.2929 1.70711L13.9393 1.35355V1.35355L14.2929 1.70711ZM15 3H12.5V4H15V3ZM12.8536 3.85355L14.6464 2.06066L13.9393 1.35355L12.1464 3.14645L12.8536 3.85355ZM13.7929 0H13.5V1H13.7929V0ZM13.5 0C12.6716 0 12 0.671573 12 1.5H13C13 1.22386 13.2239 1 13.5 1V0ZM15 1.20711C15 0.54044 14.4596 0 13.7929 0V1C13.9073 1 14 1.09272 14 1.20711H15ZM14.6464 2.06066C14.8728 1.83428 15 1.52725 15 1.20711H14C14 1.26204 13.9782 1.31471 13.9393 1.35355L14.6464 2.06066ZM1.1 1.8L10.1 13.8L10.9 13.2L1.9 1.2L1.1 1.8ZM10.1 1.2L1.1 13.2L1.9 13.8L10.9 1.8L10.1 1.2Z" fill="{color}"/> 
  {:else}
    <path fill-rule="evenodd" clip-rule="evenodd" d="M12 1.5C12 0.671573 12.6716 0 13.5 0H13.7929C14.4596 0 15 0.54044 15 1.20711C15 1.52725 14.8728 1.83428 14.6465 2.06066L13.7071 3H15V4H12.5C12.2978 4 12.1155 3.87818 12.0381 3.69134C11.9607 3.5045 12.0035 3.28945 12.1465 3.14645L13.9393 1.35355C13.9782 1.31471 14 1.26204 14 1.20711C14 1.09272 13.9073 1 13.7929 1H13.5C13.2239 1 13 1.22386 13 1.5H12ZM5.37501 7.5L1.10001 1.8L1.90001 1.2L6.00001 6.66667L10.1 1.2L10.9 1.8L6.62501 7.5L10.9 13.2L10.1 13.8L6.00001 8.33333L1.90001 13.8L1.10001 13.2L5.37501 7.5Z" fill="{color}"/> 
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