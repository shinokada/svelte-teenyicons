<script lang="ts">
  export let size: string = "15";
  export let role: string = "img";
  export let color: string = "currentColor" 
  export let variation: "solid" | "outline" = "outline";
export let ariaLabel="google ad" </script>

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
    <path d="M3.5 10V7C3.5 6.17157 4.17157 5.5 5 5.5C5.82843 5.5 6.5 6.17157 6.5 7V10M11.5 5V10M11.5 7.5H9.5C8.94772 7.5 8.5 7.94772 8.5 8.5C8.5 9.05228 8.94772 9.5 9.5 9.5H11.5M3.5 8.5H6.5M2.5 2.5H12.5C13.6046 2.5 14.5 3.39543 14.5 4.5V10.5C14.5 11.6046 13.6046 12.5 12.5 12.5H2.5C1.39543 12.5 0.5 11.6046 0.5 10.5V4.5C0.5 3.39543 1.39543 2.5 2.5 2.5Z" stroke="{color}"/> 
  {:else}
    <path d="M5 6C4.44772 6 4 6.44772 4 7V8H6V7C6 6.44772 5.55228 6 5 6Z" fill="{color}"/> <path d="M11 8H9.5C9.22386 8 9 8.22386 9 8.5C9 8.77614 9.22386 9 9.5 9H11V8Z" fill="{color}"/> <path fill-rule="evenodd" clip-rule="evenodd" d="M0 4.5C0 3.11929 1.11929 2 2.5 2H12.5C13.8807 2 15 3.11929 15 4.5V10.5C15 11.8807 13.8807 13 12.5 13H2.5C1.11929 13 0 11.8807 0 10.5V4.5ZM4 10V9H6V10H7V7C7 5.89543 6.10457 5 5 5C3.89543 5 3 5.89543 3 7V10H4ZM11 7H9.5C8.67157 7 8 7.67157 8 8.5C8 9.32843 8.67157 10 9.5 10H12V5H11V7Z" fill="{color}"/> 
  {/if}
</svg>
