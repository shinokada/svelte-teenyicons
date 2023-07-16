<script lang="ts">
  export let size: string = '15';
  export let role: string = 'img';
  export let color: string = 'currentColor';
  export let variation: 'solid' | 'outline' = 'outline';
  export let ariaLabel = 'folders';
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
      d="M3.5 8.5V1.5C3.5 0.947715 3.94772 0.5 4.5 0.5H7.5L9.5 2.5H13.5C14.0523 2.5 14.5 2.94772 14.5 3.5V8.5C14.5 9.05228 14.0523 9.5 13.5 9.5H4.5M3.5 8.5C3.5 9.05229 3.94772 9.5 4.5 9.5M3.5 8.5V5.5H1.5C0.947715 5.5 0.5 5.94772 0.5 6.5V13.5C0.5 14.0523 0.947715 14.5 1.5 14.5H10.5C11.0523 14.5 11.5 14.0523 11.5 13.5V9.5H4.5"
      stroke={color}
    />
  {:else}
    <path
      d="M4.5 0C3.67157 0 3 0.671573 3 1.5V8.5C3 9.32843 3.67157 10 4.5 10H13.5C14.3284 10 15 9.32843 15 8.5V3.5C15 2.67157 14.3284 2 13.5 2H9.70711L7.70711 0H4.5Z"
      fill={color}
    />
    <path
      d="M12 11H4.5C3.11929 11 2 9.88071 2 8.5V5H1.5C0.671573 5 0 5.67157 0 6.5V13.5C0 14.3284 0.671573 15 1.5 15H10.5C11.3284 15 12 14.3284 12 13.5V11Z"
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
