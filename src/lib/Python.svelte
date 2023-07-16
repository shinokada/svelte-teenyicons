<script lang="ts">
  export let size: string = '15';
  export let role: string = 'img';
  export let color: string = 'currentColor';
  export let variation: 'solid' | 'outline' = 'outline';
  export let ariaLabel = 'python';
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
      d="M6 2.5H7M4.5 4V1.5C4.5 0.947715 4.94772 0.5 5.5 0.5H9.5C10.0523 0.5 10.5 0.947715 10.5 1.5V6.5C10.5 7.05228 10.0523 7.5 9.5 7.5H5.5C4.94772 7.5 4.5 7.94772 4.5 8.5V13.5C4.5 14.0523 4.94772 14.5 5.5 14.5H9.5C10.0523 14.5 10.5 14.0523 10.5 13.5V11M8 4.5H1.5C0.947715 4.5 0.5 4.94772 0.5 5.5V10.5C0.5 11.0523 0.947715 11.5 1.5 11.5H4.5M7 10.5H13.5C14.0523 10.5 14.5 10.0523 14.5 9.5V4.5C14.5 3.94772 14.0523 3.5 13.5 3.5H10.5M8 12.5H9"
      stroke={color}
    />
  {:else}
    <path
      d="M3 12H1.5C0.671573 12 0 11.3284 0 10.5V5.5C0 4.67157 0.671573 4 1.5 4H8V3H7V2H6V3H4V1.5C4 0.671573 4.67157 0 5.5 0H9.5C10.3284 0 11 0.671573 11 1.5V6.5C11 6.77614 10.7761 7 10.5 7H4.5C3.67157 7 3 7.67157 3 8.5V12Z"
      fill={color}
    />
    <path
      d="M12 3V6.5C12 7.32843 11.3284 8 10.5 8H4.5C4.22386 8 4 8.22386 4 8.5V13.5C4 14.3284 4.67157 15 5.5 15H9.5C10.3284 15 11 14.3284 11 13.5V12H9V13H8V12H7V11H13.5C14.3284 11 15 10.3284 15 9.5V4.5C15 3.67157 14.3284 3 13.5 3H12Z"
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
