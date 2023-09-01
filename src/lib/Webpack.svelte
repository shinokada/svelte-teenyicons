<script lang="ts">
  export let size: string = "15";
  export let role: string = "img";
  export let color: string = "currentColor" 
  export let variation: "solid" | "outline" = "outline";
export let ariaLabel="webpack" </script>

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
    <path d="M1.5 10.5V4.5M1.5 10.5L7.5 14M1.5 10.5L5 9M1.5 4.5L7.5 1M1.5 4.5L7.5 7.5M7.5 1L13.5 4.5M7.5 1V4.5M13.5 4.5V10.5M13.5 4.5L7.5 7.5M13.5 10.5L7.5 14M13.5 10.5L10 9M7.5 14V7.5M7.5 4.5L5 6V9M7.5 4.5L10 6V9M5 9L7.5 10.5L10 9" stroke="{color}"/> 
  {:else}
    <path d="M8 4.21689L10.2491 5.56637L13.5183 3.93181L8 0.71283V4.21689Z" fill="{color}"/> <path d="M7 0.71283L1.48172 3.93183L4.75084 5.56639L7 4.21689V0.71283Z" fill="{color}"/> <path d="M1 4.809V10.2306L4.5 8.67506V6.559L1 4.809Z" fill="{color}"/> <path d="M1.5232 11.0924L7 14.2872V10.7831L4.9656 9.56244L1.5232 11.0924Z" fill="{color}"/> <path d="M8 14.2872L13.4768 11.0924L10.0344 9.56247L8 10.7831V14.2872Z" fill="{color}"/> <path d="M14 10.2307V4.80897L10.5 6.55897V8.67511L14 10.2307Z" fill="{color}"/> <path d="M8 9.61689L9.5 8.71689V7.05897L8 7.80897V9.61689Z" fill="{color}"/> <path d="M7 7.809V9.61689L5.5 8.71689V7.059L7 7.809Z" fill="{color}"/> <path d="M5.81101 6.09647L7.49997 6.94095L9.18896 6.09646L7.5 5.08308L5.81101 6.09647Z" fill="{color}"/> 
  {/if}
</svg>
