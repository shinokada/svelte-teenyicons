<script lang="ts">
  export let size: string = '15';
  export let color: string = 'black';
  export let variation: 'solid' | 'outline' = 'outline';
  export let ariaLabel = 'mood frown';
</script>

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
    <path
      d="M5.29022 10.1873L4.86642 10.4526L5.39707 11.3002L5.82087 11.0349L5.29022 10.1873ZM10.1875 9.94325L10.6863 9.97792L10.7557 8.98033L10.2569 8.94566L10.1875 9.94325ZM5.82087 11.0349C7.1245 10.2188 8.65319 9.83658 10.1875 9.94325L10.2569 8.94566C8.51172 8.82433 6.77298 9.25902 5.29022 10.1873L5.82087 11.0349ZM4 6H5V5H4V6ZM10 6H11V5H10V6ZM7.5 14C3.91015 14 1 11.0899 1 7.5H0C0 11.6421 3.35786 15 7.5 15V14ZM14 7.5C14 11.0899 11.0899 14 7.5 14V15C11.6421 15 15 11.6421 15 7.5H14ZM7.5 1C11.0899 1 14 3.91015 14 7.5H15C15 3.35786 11.6421 0 7.5 0V1ZM7.5 0C3.35786 0 0 3.35786 0 7.5H1C1 3.91015 3.91015 1 7.5 1V0Z"
      fill={color}
    />
  {:else}
    <path
      fill-rule="evenodd"
      clip-rule="evenodd"
      d="M0 7.5C0 3.35786 3.35786 0 7.5 0C11.6421 0 15 3.35786 15 7.5C15 11.6421 11.6421 15 7.5 15C3.35786 15 0 11.6421 0 7.5ZM4 6H5V5H4V6ZM5.8209 11.0349C7.12453 10.2188 8.65322 9.83658 10.1876 9.94325L10.6864 9.97792L10.7557 8.98033L10.2569 8.94566C8.51175 8.82433 6.77301 9.25902 5.29025 10.1873L4.86646 10.4526L5.3971 11.3002L5.8209 11.0349ZM11 6H10V5H11V6Z"
      fill={color}
    />
  {/if}
</svg>

<!--
  @component
  [Go to Document](https://svelte-teenyicons.codewithshin.com/)

  ## Props
  @prop size: string = "15";
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
