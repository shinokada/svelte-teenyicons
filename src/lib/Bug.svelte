<script lang="ts">
  export let size: string = '15';
  export let role: string = 'img';
  export let color: string = 'currentColor';
  export let variation: 'solid' | 'outline' = 'outline';
  export let ariaLabel = 'bug';
</script>

<svg
  xmlns="http://www.w3.org/2000/svg"
  width={size}
  height={size}
  fill="none"
  {...$$restProps}
  {role}
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
      d="M4.5 4.5H10.5M4.5 4.5L4.13344 5.23313C3.71687 6.06626 3.5 6.98494 3.5 7.91641V10.5C3.5 12.7091 5.29086 14.5 7.5 14.5C9.70914 14.5 11.5 12.7091 11.5 10.5V7.91641C11.5 6.98494 11.2831 6.06626 10.8666 5.23313L10.5 4.5M4.5 4.5V3.5C4.5 1.84315 5.84315 0.5 7.5 0.5C9.15685 0.5 10.5 1.84315 10.5 3.5V4.5M0 8.5H3.5M15 8.5H11.5M1 14L4 12.5M14 14L11 12.5M1 3L4 4.5M14 3L11 4.5"
      stroke={color}
    />
  {:else}
    <path
      fill-rule="evenodd"
      clip-rule="evenodd"
      d="M4 3.941V3.5C4 1.567 5.567 0 7.5 0C9.433 0 11 1.567 11 3.5V3.94098L13.7764 2.5528L14.2236 3.44722L11.2708 4.9236L11.3138 5.00952C11.7651 5.91208 12 6.90732 12 7.91641V8H15V9H12V10.5C12 11.1253 11.8725 11.7208 11.642 12.262L14.2236 13.5528L13.7764 14.4472L11.1492 13.1337C10.3318 14.2643 9.00182 15 7.5 15C5.99817 15 4.66818 14.2643 3.85076 13.1336L1.22358 14.4472L0.776367 13.5528L3.35803 12.262C3.12754 11.7208 3 11.1253 3 10.5V9H0V8H3V7.91641C3 6.90731 3.23494 5.91208 3.68622 5.00952L3.72917 4.92362L0.776367 3.44722L1.22358 2.5528L4 3.941ZM5 3.5C5 2.11929 6.11929 1 7.5 1C8.88071 1 10 2.11929 10 3.5V4H5V3.5Z"
      fill={color}
    />
  {/if}
</svg>

<!--
  @component
  [Go to Document](https://svelte-teenyicons.codewithshin.com/)

  ## Props
  @prop size: string = "15";
  @prop role: string = "icon file name";
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
