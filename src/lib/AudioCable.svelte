<script lang="ts">
  export let size: string = '15';
  export let role: string = 'img';
  export let color: string = 'currentColor';
  export let variation: 'solid' | 'outline' = 'outline';
  export let ariaLabel = 'audio cable';
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
      d="M6.5 1.5L6.14645 1.14645C6.05268 1.24021 6 1.36739 6 1.5H6.5ZM7.5 0.5L7.85355 0.146447C7.65829 -0.0488155 7.34171 -0.0488155 7.14645 0.146447L7.5 0.5ZM8.5 1.5H9C9 1.36739 8.94732 1.24021 8.85355 1.14645L8.5 1.5ZM6.5 9H8.5V8H6.5V9ZM9 9.5V12.5H10V9.5H9ZM8.5 13H6.5V14H8.5V13ZM6 12.5V9.5H5V12.5H6ZM6.5 13C6.22386 13 6 12.7761 6 12.5H5C5 13.3284 5.67157 14 6.5 14V13ZM9 12.5C9 12.7761 8.77614 13 8.5 13V14C9.32843 14 10 13.3284 10 12.5H9ZM8.5 9C8.77614 9 9 9.22386 9 9.5H10C10 8.67157 9.32843 8 8.5 8V9ZM6.5 8C5.67157 8 5 8.67157 5 9.5H6C6 9.22386 6.22386 9 6.5 9V8ZM7 8.5V3.5H6V8.5H7ZM6.5 4H8.5V3H6.5V4ZM8 3.5V8.5H9V3.5H8ZM7 13V15H8V13H7ZM7 3.5V1.5H6V3.5H7ZM6.85355 1.85355L7.85355 0.853553L7.14645 0.146447L6.14645 1.14645L6.85355 1.85355ZM7.14645 0.853553L8.14645 1.85355L8.85355 1.14645L7.85355 0.146447L7.14645 0.853553ZM8 1.5V3.5H9V1.5H8Z"
      fill={color}
    />
  {:else}
    <path
      d="M7.85355 0.146447C7.65829 -0.0488155 7.34171 -0.0488155 7.14645 0.146447L6.14645 1.14645C6.05268 1.24021 6 1.36739 6 1.5V3H9V1.5C9 1.36739 8.94732 1.24021 8.85355 1.14645L7.85355 0.146447Z"
      fill={color}
    /> <path d="M9 4V8H6V4H9Z" fill={color} />
    <path
      d="M10 9V12.5C10 13.3284 9.32843 14 8.5 14H8V15H7V14H6.5C5.67157 14 5 13.3284 5 12.5V9H10Z"
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
