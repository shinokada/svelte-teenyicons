<script lang="ts">
  export let size: string = '15';
  export let color: string = 'black';
  export let variation: 'solid' | 'outline' = 'outline';
  export let ariaLabel = 'phonecall';
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
      d="M14.5 0.5L8.5 6.5M14.5 0.5V4M14.5 0.5L11 0.5M2.5 0.5H4.71922C5.17809 0.5 5.57807 0.812298 5.68937 1.25746L6.2754 3.60162C6.40214 4.10855 6.11721 4.6276 5.62149 4.79284L4.51286 5.16238C3.93422 5.35526 3.58976 5.94882 3.70938 6.54691C4.18814 8.94071 6.05929 10.8119 8.45309 11.2906C9.05118 11.4102 9.64474 11.0658 9.83762 10.4871L10.1354 9.59384C10.3278 9.01652 10.987 8.74349 11.5313 9.01564L13.9472 10.2236C14.286 10.393 14.5 10.7393 14.5 11.118V12.5C14.5 13.6046 13.6046 14.5 12.5 14.5H10.5C4.97715 14.5 0.5 10.0228 0.5 4.5V2.5C0.5 1.39543 1.39543 0.5 2.5 0.5Z"
      stroke={color}
    />
  {:else}
    <path
      d="M15 0H11V1L13.2929 1L8.14645 6.14645L8.85355 6.85355L14 1.70711V4H15V0Z"
      fill={color}
    />
    <path
      d="M2.5 0C1.11929 0 0 1.11929 0 2.5V4.5C0 10.299 4.70101 15 10.5 15H12.5C13.8807 15 15 13.8807 15 12.5V11.118C15 10.5499 14.679 10.0305 14.1708 9.77639L11.7549 8.56843C10.9384 8.1602 9.94971 8.56975 9.66105 9.43573L9.36328 10.329C9.25014 10.6684 8.90197 10.8705 8.55114 10.8003C6.35528 10.3612 4.63885 8.64472 4.19967 6.44886C4.12951 6.09803 4.33156 5.74986 4.67097 5.63672L5.7796 5.26718C6.52319 5.01932 6.95058 4.24075 6.76048 3.48035L6.17444 1.1362C6.0075 0.468446 5.40752 0 4.71922 0H2.5Z"
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
