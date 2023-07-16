<script lang="ts">
  export let size: string = '15';
  export let role: string = 'img';
  export let color: string = 'currentColor';
  export let variation: 'solid' | 'outline' = 'outline';
  export let ariaLabel = 'watch';
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
      d="M4.5 3.5H10.5M4.5 3.5C3.94772 3.5 3.5 3.94772 3.5 4.5V10.5C3.5 11.0523 3.94772 11.5 4.5 11.5M4.5 3.5V1.5C4.5 0.947715 4.94772 0.5 5.5 0.5H9.5C10.0523 0.5 10.5 0.947715 10.5 1.5V3.5M10.5 3.5C11.0523 3.5 11.5 3.94772 11.5 4.5V10.5C11.5 11.0523 11.0523 11.5 10.5 11.5M10.5 11.5H4.5M10.5 11.5V13.5C10.5 14.0523 10.0523 14.5 9.5 14.5H5.5C4.94772 14.5 4.5 14.0523 4.5 13.5V11.5M13.5 6V9"
      stroke={color}
    />
  {:else}
    <path
      fill-rule="evenodd"
      clip-rule="evenodd"
      d="M4 3.08535V1.5C4 0.671573 4.67157 0 5.5 0H9.5C10.3284 0 11 0.671573 11 1.5V3.08535C11.5826 3.29127 12 3.84689 12 4.5V10.5C12 11.1531 11.5826 11.7087 11 11.9146V13.5C11 14.3284 10.3284 15 9.5 15H5.5C4.67157 15 4 14.3284 4 13.5V11.9146C3.4174 11.7087 3 11.1531 3 10.5V4.5C3 3.84689 3.4174 3.29127 4 3.08535ZM5 1.5C5 1.22386 5.22386 1 5.5 1H9.5C9.77614 1 10 1.22386 10 1.5V3H5V1.5ZM5 12H10V13.5C10 13.7761 9.77614 14 9.5 14H5.5C5.22386 14 5 13.7761 5 13.5V12Z"
      fill={color}
    /> <path d="M13 6V9H14V6H13Z" fill={color} />
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
