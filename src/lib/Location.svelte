<script lang="ts">
  export let size: string = "15";
  export let role: string = "img";
  export let color: string = "currentColor" 
  export let variation: "solid" | "outline" = "outline";
export let ariaLabel="location" </script>

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
    <path d="M7.5 0.5V14.5M14.5 7.49548H0.5M13.5 7.49548C13.5 10.8063 10.813 13.5 7.5 13.5C4.187 13.5 1.5 10.8063 1.5 7.49548C1.5 4.18464 4.187 1.49939 7.5 1.49939C10.813 1.49939 13.5 4.18464 13.5 7.49548Z" stroke="{color}" stroke-linecap="square"/> 
  {:else}
    <path fill-rule="evenodd" clip-rule="evenodd" d="M8 1.01834V0H7V1.01834C3.80973 1.26103 1.26197 3.80671 1.01898 6.99548H0V7.99548H1.01898C1.26193 11.1843 3.80902 13.7376 7 13.981V15H8V13.981C11.191 13.7376 13.7381 11.1843 13.981 7.99548H15V6.99548H13.981C13.738 3.80671 11.1903 1.26103 8 1.01834ZM8 3V6.99548H12V7.99548H8V12H7V7.99548H3V6.99548H7V3H8Z" fill="{color}"/> 
  {/if}
</svg>
