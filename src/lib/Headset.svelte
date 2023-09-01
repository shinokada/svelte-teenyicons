<script lang="ts">
  export let size: string = "15";
  export let role: string = "img";
  export let color: string = "currentColor" 
  export let variation: "solid" | "outline" = "outline";
export let ariaLabel="headset" </script>

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
    <path d="M12.5 12.5C13.6046 12.5 14.5 11.6046 14.5 10.5V8.5C14.5 7.39543 13.6046 6.5 12.5 6.5C11.9477 6.5 11.5 6.94772 11.5 7.5V11.5C11.5 12.0523 11.9477 12.5 12.5 12.5ZM12.5 12.5C12.5 13.6046 11.6046 14.5 10.5 14.5H8M14.5 10V7.5C14.5 3.63401 11.366 0.5 7.5 0.5C3.63401 0.5 0.5 3.63401 0.5 7.5V10M2.5 12.5C3.05228 12.5 3.5 12.0523 3.5 11.5V7.5C3.5 6.94772 3.05228 6.5 2.5 6.5C1.39543 6.5 0.5 7.39543 0.5 8.5V10.5C0.5 11.6046 1.39543 12.5 2.5 12.5Z" stroke="{color}"/> 
  {:else}
    <path d="M2.5 6C1.97535 6 1.48846 6.16161 1.08637 6.43776C1.5934 3.3532 4.27189 1 7.5 1C10.7281 1 13.4066 3.3532 13.9136 6.43777C13.5115 6.16161 13.0246 6 12.5 6C11.6716 6 11 6.67157 11 7.5V11.5C11 12.1333 11.3925 12.6749 11.9475 12.895C11.7741 13.5318 11.1917 14 10.5 14H8V15H10.5C11.7242 15 12.7429 14.12 12.9581 12.9581C14.12 12.7429 15 11.7242 15 10.5V7.5C15 3.35786 11.6421 0 7.5 0C3.35786 0 0 3.35786 0 7.5V10.5C0 11.8807 1.11929 13 2.5 13C3.32843 13 4 12.3284 4 11.5V7.5C4 6.67157 3.32843 6 2.5 6Z" fill="{color}"/> 
  {/if}
</svg>
