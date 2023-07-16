<script lang="ts">
  export let size: string = '15';
  export let role: string = 'img';
  export let color: string = 'currentColor';
  export let variation: 'solid' | 'outline' = 'outline';
  export let ariaLabel = 'stamp';
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
      d="M0 14.5H15M6.5 6.5V9.5M8.5 6.5V9.5M7.5 6.5C5.84315 6.5 4.5 5.15685 4.5 3.5C4.5 1.84315 5.84315 0.5 7.5 0.5C9.15685 0.5 10.5 1.84315 10.5 3.5C10.5 5.15685 9.15685 6.5 7.5 6.5ZM0.5 12.5V11.5C0.5 10.3954 1.39543 9.5 2.5 9.5H12.5C13.6046 9.5 14.5 10.3954 14.5 11.5V12.5H0.5Z"
      stroke={color}
    />
  {:else}
    <path
      d="M4 3.5C4 1.567 5.567 0 7.5 0C9.433 0 11 1.567 11 3.5C11 4.8962 10.1825 6.10145 9 6.66318V9H12.5C13.8807 9 15 10.1193 15 11.5V13H0V11.5C0 10.1193 1.11929 9 2.5 9H6V6.66318C4.81753 6.10145 4 4.8962 4 3.5Z"
      fill={color}
    /> <path d="M0 14V15H15V14H0Z" fill={color} />
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
