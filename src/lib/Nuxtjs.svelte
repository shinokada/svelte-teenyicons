<script lang="ts">
  export let size: string = '15';
  export let color: string = 'black';
  export let variation: 'solid' | 'outline' = 'outline';
  export let ariaLabel = 'nuxtjs';
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
    <path d="M0.5 12.5L6.5 2.5L12.5 12.5H0.5Z" stroke={color} stroke-linejoin="round" />
    <path d="M4.5 12.5L9.5 4L14.5 12.5H4.5Z" stroke={color} stroke-linejoin="round" />
  {:else}
    <path
      fill-rule="evenodd"
      clip-rule="evenodd"
      d="M6.5 2C6.67563 2 6.83838 2.09215 6.92875 2.24275L8.45614 4.78841L9.06903 3.74649C9.15887 3.59377 9.32282 3.5 9.5 3.5C9.67718 3.5 9.84113 3.59377 9.93097 3.74649L14.931 12.2465C15.0219 12.4011 15.0231 12.5925 14.934 12.7482C14.845 12.9039 14.6794 13 14.5 13H0.5C0.319864 13 0.153653 12.9031 0.0649001 12.7463C-0.0238527 12.5896 -0.0214256 12.3972 0.0712536 12.2428L6.07125 2.24275C6.16162 2.09215 6.32437 2 6.5 2ZM5.37421 12H11.6169L8.46465 6.74625L5.37421 12ZM7.87882 5.76986L4.21403 12H1.3831L6.5 3.47183L7.87882 5.76986ZM9.04197 5.7648L12.7831 12H13.6258L9.5 4.98615L9.04197 5.7648Z"
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
  @prop ariaLabel = 'icon file name';
  ## Event
  - on:click 
  - on:mouseenter 
  - on:mouseleave 
  - on:mouseover 
  - on:mouseout 
  - on:blur 
  - on:focus 
-->
