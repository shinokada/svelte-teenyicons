<script lang="ts">
  export let size: string = "15";
  export let color: string = "black" 
  export let variation: "solid" | "outline" = "outline";
export let ariaLabel="home alt" </script>

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
    <path d="M7.5 0.5L7.85355 0.146447C7.65829 -0.0488155 7.34171 -0.0488155 7.14645 0.146447L7.5 0.5ZM1.5 6.5L1.14645 6.14645L1 6.29289V6.5H1.5ZM13.5 6.5H14V6.29289L13.8536 6.14645L13.5 6.5ZM13.8536 6.14645L7.85355 0.146447L7.14645 0.853553L13.1464 6.85355L13.8536 6.14645ZM7.14645 0.146447L1.14645 6.14645L1.85355 6.85355L7.85355 0.853553L7.14645 0.146447ZM14 13.5V6.5H13V13.5H14ZM1 6.5V13.5H2V6.5H1ZM2.5 15H12.5V14H2.5V15ZM13 13.5C13 13.7761 12.7761 14 12.5 14V15C13.3284 15 14 14.3284 14 13.5H13ZM1 13.5C1 14.3284 1.67157 15 2.5 15V14C2.22386 14 2 13.7761 2 13.5H1Z" fill="{color}"/> 
  {:else}
    <path d="M7.85355 0.146447C7.65829 -0.0488155 7.34171 -0.0488155 7.14645 0.146447L1 6.29289V13.5C1 14.3284 1.67157 15 2.5 15H12.5C13.3284 15 14 14.3284 14 13.5V6.29289L7.85355 0.146447Z" fill="{color}"/> 
  {/if}
</svg>
