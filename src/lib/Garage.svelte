<script lang="ts">
  export let size: string = "15";
  export let role: string = "img";
  export let color: string = "currentColor" 
  export let variation: "solid" | "outline" = "outline";
export let ariaLabel="garage" </script>

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
    <path d="M0.5 5.5L0.209381 5.09313C0.0779828 5.18699 0 5.33852 0 5.5H0.5ZM7.5 0.5L7.79062 0.0931333C7.61677 -0.0310444 7.38323 -0.0310444 7.20938 0.0931333L7.5 0.5ZM14.5 5.5H15C15 5.33852 14.922 5.18699 14.7906 5.09313L14.5 5.5ZM2.5 7.5V7H2V7.5H2.5ZM12.5 7.5H13V7H12.5V7.5ZM1 15V5.5H0V15H1ZM0.790619 5.90687L7.79062 0.906867L7.20938 0.0931333L0.209381 5.09313L0.790619 5.90687ZM7.20938 0.906867L14.2094 5.90687L14.7906 5.09313L7.79062 0.0931333L7.20938 0.906867ZM14 5.5V15H15V5.5H14ZM3 15V7.5H2V15H3ZM2.5 8H12.5V7H2.5V8ZM12 7.5V15H13V7.5H12ZM2.5 11H12.5V10H2.5V11ZM6 13H9V12H6V13Z" fill="{color}"/> 
  {:else}
    <path d="M7.20938 0.0931333C7.38323 -0.0310444 7.61677 -0.0310444 7.79062 0.0931333L14.7906 5.09313C14.922 5.18699 15 5.33852 15 5.5V14.5C15 14.7761 14.7761 15 14.5 15H13V7H2V15H0.5C0.223858 15 0 14.7761 0 14.5V5.5C0 5.33852 0.0779828 5.18699 0.209381 5.09313L7.20938 0.0931333Z" fill="{color}"/> <path fill-rule="evenodd" clip-rule="evenodd" d="M3 15H12V11H3V15ZM9 13H6V12H9V13Z" fill="{color}"/> <path d="M12 10V8H3V10H12Z" fill="{color}"/> 
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