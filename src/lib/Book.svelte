<script lang="ts">
  export let size: string = "15";
  export let role: string = "img";
  export let color: string = "currentColor" 
  export let variation: "solid" | "outline" = "outline";
export let ariaLabel="book" </script>

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
    <path d="M1.5 0.5V0C1.22386 0 1 0.223858 1 0.5H1.5ZM1.5 13.5H1C1 13.7761 1.22386 14 1.5 14V13.5ZM4 0V15H5V0H4ZM1.5 1H11.5V0H1.5V1ZM13 2.5V11.5H14V2.5H13ZM11.5 13H1.5V14H11.5V13ZM2 13.5V0.5H1V13.5H2ZM13 11.5C13 12.3284 12.3284 13 11.5 13V14C12.8807 14 14 12.8807 14 11.5H13ZM11.5 1C12.3284 1 13 1.67157 13 2.5H14C14 1.11929 12.8807 0 11.5 0V1ZM7 5H11V4H7V5Z" fill="{color}"/> 
  {:else}
    <path d="M1.5 0C1.22386 0 1 0.223858 1 0.5V13.5C1 13.7761 1.22386 14 1.5 14H3V0H1.5Z" fill="{color}"/> <path fill-rule="evenodd" clip-rule="evenodd" d="M4 15H5V14H11.5C12.8807 14 14 12.8807 14 11.5V2.5C14 1.11929 12.8807 0 11.5 0H4V15ZM11 5H7V4H11V5Z" fill="{color}"/> 
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