<script lang="ts">
  export let size: string = "15";
  export let role: string = "img";
  export let color: string = "currentColor" 
  export let variation: "solid" | "outline" = "outline";
export let ariaLabel="church" </script>

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
    <path d="M3 8.5C3 8.22386 2.77614 8 2.5 8C2.22386 8 2 8.22386 2 8.5H3ZM13 8.5C13 8.22386 12.7761 8 12.5 8C12.2239 8 12 8.22386 12 8.5H13ZM5.5 10.5V10H5V10.5H5.5ZM9.5 10.5H10V10H9.5V10.5ZM0 15H15V14H0V15ZM7.25193 5.06588L0.251931 9.06588L0.748069 9.93412L7.74807 5.93412L7.25193 5.06588ZM14.7481 9.06588L7.74807 5.06588L7.25193 5.93412L14.2519 9.93412L14.7481 9.06588ZM7 0V2.5H8V0H7ZM7 2.5V5.5H8V2.5H7ZM5 3H7.5V2H5V3ZM7.5 3H10V2H7.5V3ZM2 8.5V14.5H3V8.5H2ZM12 8.5V14.5H13V8.5H12ZM6 14.5V10.5H5V14.5H6ZM5.5 11H9.5V10H5.5V11ZM9 10.5V14.5H10V10.5H9Z" fill="{color}"/> 
  {:else}
    <path d="M7 2V0H8V2H10V3H8V5.20983L14.7481 9.06589L14.252 9.93413L13 9.21873V14H15V15H10V10H5V15H0V14H2V9.21875L0.748092 9.93413L0.251953 9.06589L7 5.20986V3H5V2H7Z" fill="{color}"/> <path d="M6 15H9V11H6V15Z" fill="{color}"/> 
  {/if}
</svg>
