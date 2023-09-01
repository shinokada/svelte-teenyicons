<script lang="ts">
  export let size: string = "15";
  export let role: string = "img";
  export let color: string = "currentColor" 
  export let variation: "solid" | "outline" = "outline";
export let ariaLabel="android" </script>

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
    <path d="M2.5 2.5L4.5 5.5M12.5 2.5L10.5 5.5M4 9.5H5M10 9.5H11M1.5 12.5V10.5C1.5 7.18629 4.18629 4.5 7.5 4.5C10.8137 4.5 13.5 7.18629 13.5 10.5V12.5H1.5Z" stroke="{color}"/> 
  {:else}
    <path fill-rule="evenodd" clip-rule="evenodd" d="M7.5 4C6.44445 4 5.44766 4.25161 4.56634 4.69812L2.91603 2.22266L2.08398 2.77736L3.71104 5.21794C2.06927 6.39771 1 8.32399 1 10.5V13H14V10.5C14 8.32399 12.9307 6.39772 11.289 5.21795L12.916 2.77736L12.084 2.22266L10.4337 4.69812C9.55235 4.25161 8.55556 4 7.5 4ZM5 10H4V9H5V10ZM10 10H11V9H10V10Z" fill="{color}"/> 
  {/if}
</svg>
