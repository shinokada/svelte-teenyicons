<script lang="ts">
  export let size: string = "15";
  export let role: string = "img";
  export let color: string = "currentColor" 
  export let variation: "solid" | "outline" = "outline";
export let ariaLabel="mouse" </script>

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
    <path d="M7.5 4V7M7.5 14.5C4.73858 14.5 2.5 12.2614 2.5 9.5V5.5C2.5 2.73858 4.73858 0.5 7.5 0.5C10.2614 0.5 12.5 2.73858 12.5 5.5V9.5C12.5 12.2614 10.2614 14.5 7.5 14.5Z" stroke="{color}"/> 
  {:else}
    <path fill-rule="evenodd" clip-rule="evenodd" d="M2 5.5C2 2.46243 4.46243 0 7.5 0C10.5376 0 13 2.46243 13 5.5V9.5C13 12.5376 10.5376 15 7.5 15C4.46243 15 2 12.5376 2 9.5V5.5ZM7 4V7H8V4H7Z" fill="{color}"/> 
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