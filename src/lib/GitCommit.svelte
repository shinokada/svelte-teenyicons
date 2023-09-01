<script lang="ts">
  export let size: string = "15";
  export let role: string = "img";
  export let color: string = "currentColor" 
  export let variation: "solid" | "outline" = "outline";
export let ariaLabel="git commit" </script>

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
    <path d="M7.5 10.5C5.84315 10.5 4.5 9.15685 4.5 7.5C4.5 5.84315 5.84315 4.5 7.5 4.5M7.5 10.5C9.15685 10.5 10.5 9.15685 10.5 7.5C10.5 5.84315 9.15685 4.5 7.5 4.5M7.5 10.5V15M7.5 4.5V0" stroke="{color}"/> 
  {:else}
    <path d="M4 7.5C4 5.73676 5.30385 4.27806 7 4.03544V0H8V4.03544C9.69615 4.27806 11 5.73676 11 7.5C11 9.26324 9.69615 10.7219 8 10.9646V15H7V10.9646C5.30385 10.7219 4 9.26324 4 7.5Z" fill="{color}"/> 
  {/if}
</svg>
