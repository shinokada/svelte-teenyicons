<script lang="ts">
  export let size: string = '15';
  export let color: string = 'black';
  export let variation: 'solid' | 'outline' = 'outline';
  export let ariaLabel = 'windows';
</script>

<svg
  xmlns="http://www.w3.org/2000/svg"
  width={size}
  height={size}
  fill="none"
  class={$$props.class}
  {...$$restProps}
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
      d="M0.5 3.5L0.395235 3.0111C0.1647 3.0605 0 3.26423 0 3.5H0.5ZM14.5 0.5H15C15 0.349004 14.9318 0.206095 14.8143 0.111167C14.6969 0.0162391 14.5429 -0.0205393 14.3952 0.0110988L14.5 0.5ZM14.5 14.5L14.4293 14.995C14.5728 15.0155 14.7181 14.9727 14.8276 14.8777C14.9371 14.7828 15 14.6449 15 14.5H14.5ZM0.5 12.5H0C0 12.7488 0.182965 12.9598 0.429289 12.995L0.5 12.5ZM0.604765 3.9889L14.6048 0.988901L14.3952 0.0110988L0.395235 3.0111L0.604765 3.9889ZM14 0.5V14.5H15V0.5H14ZM14.5707 14.005L0.570711 12.005L0.429289 12.995L14.4293 14.995L14.5707 14.005ZM1 12.5V3.5H0V12.5H1ZM0.5 8H14.5V7H0.5V8ZM6 2V13H7V2H6Z"
      fill={color}
    />
  {:else}
    <path
      d="M14.8143 0.111171C14.9318 0.206099 15 0.349008 15 0.500004V7H7V1.5958L14.3952 0.0111032C14.5429 -0.0205349 14.6969 0.0162435 14.8143 0.111171Z"
      fill={color}
    />
    <path d="M6 1.81008L0.395235 3.0111C0.1647 3.0605 0 3.26424 0 3.5V7H6V1.81008Z" fill={color} />
    <path d="M0 8V12.5C0 12.7488 0.182965 12.9598 0.429289 12.995L6 13.7908V8H0Z" fill={color} />
    <path
      d="M7 13.9337L14.4293 14.995C14.5728 15.0155 14.7181 14.9727 14.8276 14.8777C14.9371 14.7828 15 14.645 15 14.5V8H7V13.9337Z"
      fill={color}
    />
  {/if}
</svg>

<!--
  @component
  [Go to Document](https://svelte-teenyicons.codewithshin.com/)

  ## Props
  @prop size: string = "15";
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
