<script lang="ts">
  export let size: string = '15';
  export let role: string = 'img';
  export let color: string = 'currentColor';
  export let variation: 'solid' | 'outline' = 'outline';
  export let ariaLabel = 'calendar no access';
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
      d="M3.5 0V5M11.5 0V5M9.5 6.5L5.5 10.5M1.5 2.5H13.5C14.0523 2.5 14.5 2.94772 14.5 3.5V13.5C14.5 14.0523 14.0523 14.5 13.5 14.5H1.5C0.947716 14.5 0.5 14.0523 0.5 13.5V3.5C0.5 2.94772 0.947715 2.5 1.5 2.5ZM7.5 11.5C5.84315 11.5 4.5 10.1569 4.5 8.5C4.5 6.84315 5.84315 5.5 7.5 5.5C9.15685 5.5 10.5 6.84315 10.5 8.5C10.5 10.1569 9.15685 11.5 7.5 11.5Z"
      stroke={color}
    />
  {:else}
    <path
      d="M7.5 6C6.11929 6 5 7.11929 5 8.5C5 9.00954 5.15244 9.48349 5.4142 9.8787L8.8787 6.4142C8.48349 6.15244 8.00954 6 7.5 6Z"
      fill={color}
    />
    <path
      d="M7.5 11C6.99046 11 6.51653 10.8476 6.12131 10.5858L9.58581 7.12131C9.84756 7.51653 10 7.99046 10 8.5C10 9.88071 8.88071 11 7.5 11Z"
      fill={color}
    />
    <path
      fill-rule="evenodd"
      clip-rule="evenodd"
      d="M13.5 2H12V0H11V2H4V0H3V2H1.5C0.671573 2 0 2.67157 0 3.5V13.5C0 14.3284 0.671573 15 1.5 15H13.5C14.3284 15 15 14.3284 15 13.5V3.5C15 2.67157 14.3284 2 13.5 2ZM4 8.5C4 6.567 5.567 5 7.5 5C9.433 5 11 6.567 11 8.5C11 10.433 9.433 12 7.5 12C5.567 12 4 10.433 4 8.5Z"
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
