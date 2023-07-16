<script lang="ts">
  export let size: string = '15';
  export let role: string = 'img';
  export let color: string = 'currentColor';
  export let variation: 'solid' | 'outline' = 'outline';
  export let ariaLabel = 'grid layout';
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
      d="M5.5 0.5H1.5C0.947715 0.5 0.5 0.947715 0.5 1.5V5.5C0.5 6.05228 0.947715 6.5 1.5 6.5H5.5C6.05228 6.5 6.5 6.05228 6.5 5.5V1.5C6.5 0.947715 6.05228 0.5 5.5 0.5Z"
      stroke={color}
    />
    <path
      d="M13.5 0.5H9.5C8.94772 0.5 8.5 0.947715 8.5 1.5V5.5C8.5 6.05228 8.94772 6.5 9.5 6.5H13.5C14.0523 6.5 14.5 6.05228 14.5 5.5V1.5C14.5 0.947715 14.0523 0.5 13.5 0.5Z"
      stroke={color}
    />
    <path
      d="M13.5 8.5H9.5C8.94772 8.5 8.5 8.94772 8.5 9.5V13.5C8.5 14.0523 8.94772 14.5 9.5 14.5H13.5C14.0523 14.5 14.5 14.0523 14.5 13.5V9.5C14.5 8.94772 14.0523 8.5 13.5 8.5Z"
      stroke={color}
    />
    <path
      d="M5.5 8.5H1.5C0.947715 8.5 0.5 8.94772 0.5 9.5V13.5C0.5 14.0523 0.947715 14.5 1.5 14.5H5.5C6.05228 14.5 6.5 14.0523 6.5 13.5V9.5C6.5 8.94772 6.05228 8.5 5.5 8.5Z"
      stroke={color}
    />
  {:else}
    <path
      d="M1.5 0C0.671573 0 0 0.671573 0 1.5V5.5C0 6.32843 0.671573 7 1.5 7H5.5C6.32843 7 7 6.32843 7 5.5V1.5C7 0.671573 6.32843 0 5.5 0H1.5Z"
      fill={color}
    />
    <path
      d="M9.5 0C8.67157 0 8 0.671573 8 1.5V5.5C8 6.32843 8.67157 7 9.5 7H13.5C14.3284 7 15 6.32843 15 5.5V1.5C15 0.671573 14.3284 0 13.5 0H9.5Z"
      fill={color}
    />
    <path
      d="M1.5 8C0.671573 8 0 8.67157 0 9.5V13.5C0 14.3284 0.671573 15 1.5 15H5.5C6.32843 15 7 14.3284 7 13.5V9.5C7 8.67157 6.32843 8 5.5 8H1.5Z"
      fill={color}
    />
    <path
      d="M9.5 8C8.67157 8 8 8.67157 8 9.5V13.5C8 14.3284 8.67157 15 9.5 15H13.5C14.3284 15 15 14.3284 15 13.5V9.5C15 8.67157 14.3284 8 13.5 8H9.5Z"
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
