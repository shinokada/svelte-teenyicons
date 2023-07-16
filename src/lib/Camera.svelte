<script lang="ts">
  export let size: string = '15';
  export let role: string = 'img';
  export let color: string = 'currentColor';
  export let variation: 'solid' | 'outline' = 'outline';
  export let ariaLabel = 'camera';
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
      d="M7 1.5L2 1.5M14.5 12.5L14.5 4.5C14.5 3.94772 14.0523 3.5 13.5 3.5L1.5 3.5C0.947717 3.5 0.500001 3.94772 0.500001 4.5L0.5 12.5C0.5 13.0523 0.947716 13.5 1.5 13.5L13.5 13.5C14.0523 13.5 14.5 13.0523 14.5 12.5ZM9.5 10.5C8.39543 10.5 7.5 9.60457 7.5 8.5C7.5 7.39543 8.39543 6.5 9.5 6.5C10.6046 6.5 11.5 7.39543 11.5 8.5C11.5 9.60457 10.6046 10.5 9.5 10.5Z"
      stroke={color}
    />
  {:else}
    <path d="M2 1H7V2L2 2V1Z" fill={color} />
    <path
      d="M8 8.5C8 7.67157 8.67157 7 9.5 7C10.3284 7 11 7.67157 11 8.5C11 9.32843 10.3284 10 9.5 10C8.67157 10 8 9.32843 8 8.5Z"
      fill={color}
    />
    <path
      fill-rule="evenodd"
      clip-rule="evenodd"
      d="M0 12.5C0 13.3284 0.671574 14 1.5 14L13.5 14C14.3284 14 15 13.3284 15 12.5L15 4.5C15 3.67158 14.3284 3 13.5 3H1.5C0.671574 3 0 3.67157 0 4.5V12.5ZM9.5 6C8.11929 6 7 7.11929 7 8.5C7 9.88071 8.11929 11 9.5 11C10.8807 11 12 9.88071 12 8.5C12 7.11929 10.8807 6 9.5 6Z"
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
