<script lang="ts">
  export let size: string = '15';
  export let role: string = 'img';
  export let color: string = 'currentColor';
  export let variation: 'solid' | 'outline' = 'outline';
  export let ariaLabel = 'mood surprised';
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
      d="M4 5.5H5M10 5.5H11M7.5 14.5C3.63401 14.5 0.5 11.366 0.5 7.5C0.5 3.63401 3.63401 0.5 7.5 0.5C11.366 0.5 14.5 3.63401 14.5 7.5C14.5 11.366 11.366 14.5 7.5 14.5ZM7 7.5H8C8.82843 7.5 9.5 8.17157 9.5 9C9.5 9.82843 8.82843 10.5 8 10.5H7C6.17157 10.5 5.5 9.82843 5.5 9C5.5 8.17157 6.17157 7.5 7 7.5Z"
      stroke={color}
    />
  {:else}
    <path
      d="M7 8C6.44772 8 6 8.44772 6 9C6 9.55228 6.44772 10 7 10H8C8.55228 10 9 9.55228 9 9C9 8.44772 8.55228 8 8 8H7Z"
      fill={color}
    />
    <path
      fill-rule="evenodd"
      clip-rule="evenodd"
      d="M0 7.5C0 3.35786 3.35786 0 7.5 0C11.6421 0 15 3.35786 15 7.5C15 11.6421 11.6421 15 7.5 15C3.35786 15 0 11.6421 0 7.5ZM4 6H5V5H4V6ZM10 6H11V5H10V6ZM5 9C5 7.89543 5.89543 7 7 7H8C9.10457 7 10 7.89543 10 9C10 10.1046 9.10457 11 8 11H7C5.89543 11 5 10.1046 5 9Z"
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
