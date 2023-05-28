<script lang="ts">
  export let size: string = "15";
  export let color: string = "black" 
  export let variation: "solid" | "outline" = "outline";
export let ariaLabel="school" </script>

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
    <path d="M7.5 4.5L11.5 6.5V14.5H3.5V6.5L7.5 4.5ZM7.5 4.5V0M0 14.5H15M1.5 14.5V8.5H3.5M13.5 14.5V8.5H11.5M6.5 14.5V11.5H8.5V14.5M7.5 0.5H10.5V2.5H7.5M7.5 9.5C6.94772 9.5 6.5 9.05228 6.5 8.5C6.5 7.94772 6.94772 7.5 7.5 7.5C8.05228 7.5 8.5 7.94772 8.5 8.5C8.5 9.05228 8.05228 9.5 7.5 9.5Z" stroke="{color}"/> 
  {:else}
    <path d="M7.5 8C7.22386 8 7 8.22386 7 8.5C7 8.77614 7.22386 9 7.5 9C7.77614 9 8 8.77614 8 8.5C8 8.22386 7.77614 8 7.5 8Z" fill="{color}"/> <path fill-rule="evenodd" clip-rule="evenodd" d="M12 6.19098L8 4.19098V3H11V0H7V4.19098L3 6.19098V8H1V14H0V15H6V11H9V15H15V14H14V8H12V6.19098ZM13 14V9H12V14H13ZM3 14H2V9H3V14ZM6 8.5C6 7.67157 6.67157 7 7.5 7C8.32843 7 9 7.67157 9 8.5C9 9.32843 8.32843 10 7.5 10C6.67157 10 6 9.32843 6 8.5Z" fill="{color}"/> <path d="M8 15V12H7V15H8Z" fill="{color}"/> 
  {/if}
</svg>
