<script lang="ts">
  export let size: string = "15";
  export let role: string = "img";
  export let color: string = "currentColor" 
  export let variation: "solid" | "outline" = "outline";
export let ariaLabel="tiktok" </script>

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
    <path d="M9.5 0V11C9.5 12.933 7.933 14.5 6 14.5C4.067 14.5 2.5 12.933 2.5 11C2.5 9.067 4.067 7.5 6 7.5M14 5.5C11.5147 5.5 9.5 3.48528 9.5 1" stroke="{color}"/> 
  {:else}
    <path fill-rule="evenodd" clip-rule="evenodd" d="M9 0H10V1C10 3.20914 11.7909 5 14 5V6C12.3644 6 10.9122 5.21466 10 4.00049V11C10 13.2091 8.20914 15 6 15C3.79086 15 2 13.2091 2 11C2 8.79086 3.79086 7 6 7V8C4.34315 8 3 9.34315 3 11C3 12.6569 4.34315 14 6 14C7.65685 14 9 12.6569 9 11V0Z" fill="{color}"/> 
  {/if}
</svg>
