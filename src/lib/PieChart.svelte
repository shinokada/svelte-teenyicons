<script lang="ts">
  export let size: string = "15";
  export let color: string = "black" 
  export let variation: "solid" | "outline" = "outline";
export let ariaLabel="pie chart" </script>

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
    <path d="M7.5 7.5H7C7 7.63261 7.05268 7.75979 7.14645 7.85355L7.5 7.5ZM7.5 14C3.91015 14 1 11.0899 1 7.5H0C0 11.6421 3.35786 15 7.5 15V14ZM14 7.5C14 11.0899 11.0899 14 7.5 14V15C11.6421 15 15 11.6421 15 7.5H14ZM7.5 1C11.0899 1 14 3.91015 14 7.5H15C15 3.35786 11.6421 0 7.5 0V1ZM7.5 0C3.35786 0 0 3.35786 0 7.5H1C1 3.91015 3.91015 1 7.5 1V0ZM7 0V7.5H8V0H7ZM7.72361 7.94721L13.7236 4.94721L13.2764 4.05279L7.27639 7.05279L7.72361 7.94721ZM7.14645 7.85355L12.1464 12.8536L12.8536 12.1464L7.85355 7.14645L7.14645 7.85355Z" fill="{color}"/> 
  {:else}
    <path d="M7 0.0164185C3.09098 0.273712 0 3.52589 0 7.50002C0 11.6422 3.35786 15 7.5 15C9.39113 15 11.1188 14.3001 12.438 13.1451L7.15045 7.85754C7.05532 7.76453 7 7.63608 7 7.50002V0.0164185Z" fill="{color}"/> <path d="M13.1451 12.438C14.3001 11.1188 15 9.39113 15 7.50002C15 6.4718 14.7931 5.49191 14.4186 4.59972L8.3441 7.63698L13.1451 12.438Z" fill="{color}"/> <path d="M13.9708 3.70562C12.7472 1.62346 10.5473 0.18408 8 0.0164185V6.691L13.9708 3.70562Z" fill="{color}"/> 
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