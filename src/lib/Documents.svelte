<script lang="ts">
  export let size: string = '15';
  export let color: string = 'black';
  export let variation: 'solid' | 'outline' = 'outline';
  export let ariaLabel = 'documents';
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
      d="M10.5 0.5L10.7774 0.0839748L10.6514 0H10.5V0.5ZM13.5 2.5H14V2.23241L13.7774 2.08397L13.5 2.5ZM12.5 12H4.5V13H12.5V12ZM4 11.5V1.5H3V11.5H4ZM4.5 1H10.5V0H4.5V1ZM13 2.5V11.5H14V2.5H13ZM10.2226 0.916025L13.2226 2.91603L13.7774 2.08397L10.7774 0.0839748L10.2226 0.916025ZM4.5 12C4.22386 12 4 11.7761 4 11.5H3C3 12.3284 3.67157 13 4.5 13V12ZM12.5 13C13.3284 13 14 12.3284 14 11.5H13C13 11.7761 12.7761 12 12.5 12V13ZM4 1.5C4 1.22386 4.22386 1 4.5 1V0C3.67157 0 3 0.671573 3 1.5H4ZM1 3.5V13.5H2V3.5H1ZM2.5 15H10.5V14H2.5V15ZM2.5 3H3.5V2H2.5V3ZM12 13.5V12.5H11V13.5H12ZM10.5 15C11.3284 15 12 14.3284 12 13.5H11C11 13.7761 10.7761 14 10.5 14V15ZM1 13.5C1 14.3284 1.67157 15 2.5 15V14C2.22386 14 2 13.7761 2 13.5H1ZM2 3.5C2 3.22386 2.22386 3 2.5 3V2C1.67157 2 1 2.67157 1 3.5H2Z"
      fill={color}
    />
  {:else}
    <path
      fill-rule="evenodd"
      clip-rule="evenodd"
      d="M3 1.5C3 0.671572 3.67157 0 4.5 0H10.6514L14 2.23241V11.5C14 12.3284 13.3284 13 12.5 13H12V13.5C12 14.3284 11.3284 15 10.5 15H2.5C1.67157 15 1 14.3284 1 13.5V3.5C1 2.67157 1.67157 2 2.5 2H3V1.5ZM3 3H2.5C2.22386 3 2 3.22386 2 3.5V13.5C2 13.7761 2.22386 14 2.5 14H10.5C10.7761 14 11 13.7761 11 13.5V13H4.5C3.67157 13 3 12.3284 3 11.5V3Z"
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
-->
