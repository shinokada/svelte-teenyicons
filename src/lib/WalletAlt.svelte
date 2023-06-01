<script lang="ts">
  export let size: string = '15';
  export let role: string = 'img';
  export let color: string = 'black';
  export let variation: 'solid' | 'outline' = 'outline';
  export let ariaLabel = 'wallet alt';
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
      d="M13.5 6V2.5C13.5 1.94772 13.0523 1.5 12.5 1.5L1.5 1.5C0.947716 1.5 0.5 1.94772 0.5 2.5L0.5 12.5C0.5 13.0523 0.947715 13.5 1.5 13.5L12.5 13.5C13.0523 13.5 13.5 13.0523 13.5 12.5V9M14.4307 5.5H9.5C8.39543 5.5 7.5 6.39543 7.5 7.5C7.5 8.60457 8.39543 9.5 9.5 9.5H14.4307C14.469 9.5 14.5 9.46897 14.5 9.43069V5.56931C14.5 5.53103 14.469 5.5 14.4307 5.5Z"
      stroke={color}
    />
  {:else}
    <path
      fill-rule="evenodd"
      clip-rule="evenodd"
      d="M14 12.5L14 10H14.4307C14.7451 10 15 9.74511 15 9.43069V5.56931C15 5.25489 14.7451 5 14.4307 5H14V2.5C14 1.67157 13.3284 1 12.5 1H1.5C0.671574 1 0 1.67157 0 2.5V12.5C0 13.3284 0.671571 14 1.5 14H12.5C13.3284 14 14 13.3284 14 12.5ZM14 6V9L9.5 9C8.67157 9 8 8.32843 8 7.5C8 6.67157 8.67157 6 9.5 6H14Z"
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
