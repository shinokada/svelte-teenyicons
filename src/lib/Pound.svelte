<script lang="ts">
  export let size: string = "15";
  export let color: string = "black" 
  export let variation: "solid" | "outline" = "outline";
export let ariaLabel="pound" </script>

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
    <path d="M0.5 14.5L1.60263 14.1325C2.73572 13.7548 3.5 12.6944 3.5 11.5V4.44174C3.5 2.26478 5.26478 0.5 7.44174 0.5H8.30742C9.93365 0.5 11.396 1.49009 12 3M3 13H4.08359C5.01506 13 5.93374 13.2169 6.76687 13.6334L6.81672 13.6584C8.50588 14.5029 10.4941 14.5029 12.1833 13.6584L13.5 13M1 7.5H9" stroke="{color}"/> 
  {:else}
    <path fill-rule="evenodd" clip-rule="evenodd" d="M3 4.44174C3 1.98864 4.98864 0 7.44175 0H8.30742C10.1381 0 11.7843 1.11456 12.4642 2.8143L11.5358 3.1857C11.0077 1.86561 9.72919 1 8.30742 1H7.44175C5.54092 1 4 2.54092 4 4.44174V7H9V8H4V11.5C4 11.8461 3.94564 12.1826 3.84382 12.5H4.08359C5.09269 12.5 6.08792 12.7349 6.99048 13.1862L7.04032 13.2111L6.81672 13.6584L7.04033 13.2111C8.58873 13.9853 10.4113 13.9853 11.9597 13.2111L13.2764 12.5528L13.7236 13.4472L12.4069 14.1056C10.577 15.0205 8.42304 15.0205 6.59312 14.1056L6.54327 14.0807L6.76688 13.6334L6.54327 14.0807C5.77956 13.6988 4.93744 13.5 4.08359 13.5H3.31835C2.92985 14.0038 2.39412 14.3957 1.76075 14.6068L0.658116 14.9743L0.341888 14.0257L1.44452 13.6581C2.37344 13.3485 3 12.4792 3 11.5V8H1V7H3V4.44174Z" fill="{color}"/> 
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