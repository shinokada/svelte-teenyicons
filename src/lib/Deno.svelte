<script lang="ts">
  export let size: string = "15";
  export let role: string = "img";
  export let color: string = "currentColor" 
  export let variation: "solid" | "outline" = "outline";
export let ariaLabel="deno" </script>

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
    <path d="M7.5 14.5C3.63401 14.5 0.5 11.366 0.5 7.5C0.5 3.63401 3.63401 0.5 7.5 0.5C11.366 0.5 14.5 3.63401 14.5 7.5C14.5 11.366 11.366 14.5 7.5 14.5ZM7.5 14.5V9.5H6C4.61929 9.5 3.5 8.38071 3.5 7C3.5 5.61929 4.61929 4.5 6 4.5H7.69388C9.54874 4.5 11.0805 5.94903 11.1834 7.80103L11.5 13.5M7 9.5H7.38197C8.06717 9.5 8.69357 9.11287 9 8.5M4 6.5H5M6 6.5H7" stroke="{color}"/> 
  {:else}
    <path d="M7 7H6V6H7V7Z" fill="{color}"/> <path fill-rule="evenodd" clip-rule="evenodd" d="M7.5 0C3.35786 0 0 3.35786 0 7.5C0 11.6421 3.35786 15 7.5 15C11.6421 15 15 11.6421 15 7.5C15 3.35786 11.6421 0 7.5 0ZM8 13.9811C9.08703 13.8984 10.0993 13.5483 10.9713 12.9965L10.6842 7.82877C10.596 6.24172 9.28337 5 7.69388 5H6C5.25972 5 4.61337 5.4022 4.26756 6H5V7H4C4 8.10457 4.89543 9 6 9L6.88197 8.99997C7.37779 8.99997 7.83105 8.71984 8.05279 8.27637L8.94721 8.72358C8.73444 9.14912 8.40082 9.4894 8 9.71125V13.9811Z" fill="{color}"/> 
  {/if}
</svg>


<!--
  @component
  [Go to Document](https://svelte-teenyicons.codewithshin.com/)

  ## Props
  @prop size: string = "15";
  @prop role: string = "icon file name";
  @prop color: string = "black" 
  @prop variation: "solid" | "outline" = "outline";
  @prop ariaLabel = 'icon file name';
  ## Event
  - on:click 
  - on:mouseenter 
  - on:mouseleave 
  - on:mouseover 
  - on:mouseout 
  - on:blur 
  - on:focus 
-->