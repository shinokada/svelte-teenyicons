<script lang="ts">
  export let size: string = "15";
  export let role: string = "img";
  export let color: string = "currentColor" 
  export let variation: "solid" | "outline" = "outline";
export let ariaLabel="microphone" </script>

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
    <path d="M2.5 4V6.5C2.5 9.26142 4.73858 11.5 7.5 11.5M12.5 4V6.5C12.5 9.26142 10.2614 11.5 7.5 11.5M7.5 11.5V15M5 14.5H10M9.5 2.5V6.5C9.5 7.60457 8.60457 8.5 7.5 8.5C6.39543 8.5 5.5 7.60457 5.5 6.5V2.5C5.5 1.39543 6.39543 0.5 7.5 0.5C8.60457 0.5 9.5 1.39543 9.5 2.5Z" stroke="{color}"/> 
  {:else}
    <path d="M5 2.5C5 1.11929 6.11929 0 7.5 0C8.88071 0 10 1.11929 10 2.5V6.5C10 7.88071 8.88071 9 7.5 9C6.11929 9 5 7.88071 5 6.5V2.5Z" fill="{color}"/> <path d="M2 4V6.5C2 9.36902 4.19675 11.725 7 11.9776V14H5V15H10V14H8V11.9776C10.8033 11.725 13 9.36902 13 6.5V4H12V6.5C12 8.98528 9.98528 11 7.5 11C5.01472 11 3 8.98528 3 6.5V4H2Z" fill="{color}"/> 
  {/if}
</svg>
