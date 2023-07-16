<script lang="ts">
  export let size: string = '15';
  export let role: string = 'img';
  export let color: string = 'currentColor';
  export let variation: 'solid' | 'outline' = 'outline';
  export let ariaLabel = 'png';
</script>

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
    <path
      d="M2.5 6.5V6H2V6.5H2.5ZM10.5 10.5H10V11H10.5V10.5ZM12.5 10.5V11H13V10.5H12.5ZM13.5 3.5H14V3.29289L13.8536 3.14645L13.5 3.5ZM10.5 0.5L10.8536 0.146447L10.7071 0H10.5V0.5ZM6.5 6.5L6.94721 6.27639L6 6.5H6.5ZM6 10.5V11H7V10.5H6ZM8.5 10.5L8.05279 10.7236C8.15649 10.931 8.38919 11.0399 8.61488 10.9866C8.84056 10.9333 9 10.7319 9 10.5H8.5ZM9 6.5V6H8V6.5H9ZM2.5 7H3.5V6H2.5V7ZM3 11V8.5H2V11H3ZM3 8.5V6.5H2V8.5H3ZM3.5 8H2.5V9H3.5V8ZM4 7.5C4 7.77614 3.77614 8 3.5 8V9C4.32843 9 5 8.32843 5 7.5H4ZM3.5 7C3.77614 7 4 7.22386 4 7.5H5C5 6.67157 4.32843 6 3.5 6V7ZM10 6V10.5H11V6H10ZM10.5 11H12.5V10H10.5V11ZM13 10.5V8.5H12V10.5H13ZM10.5 7H13V6H10.5V7ZM2 5V1.5H1V5H2ZM13 3.5V5H14V3.5H13ZM2.5 1H10.5V0H2.5V1ZM10.1464 0.853553L13.1464 3.85355L13.8536 3.14645L10.8536 0.146447L10.1464 0.853553ZM2 1.5C2 1.22386 2.22386 1 2.5 1V0C1.67157 0 1 0.671573 1 1.5H2ZM1 12V13.5H2V12H1ZM2.5 15H12.5V14H2.5V15ZM14 13.5V12H13V13.5H14ZM12.5 15C13.3284 15 14 14.3284 14 13.5H13C13 13.7761 12.7761 14 12.5 14V15ZM1 13.5C1 14.3284 1.67157 15 2.5 15V14C2.22386 14 2 13.7761 2 13.5H1ZM6 6.5V10.5H7V6.5H6ZM6.05279 6.72361L8.05279 10.7236L8.94721 10.2764L6.94721 6.27639L6.05279 6.72361ZM8 6.5V10.5H9V6.5H8Z"
      fill={color}
    />
  {:else}
    <path d="M3 8H3.5C3.77614 8 4 7.77614 4 7.5C4 7.22386 3.77614 7 3.5 7H3V8Z" fill={color} />
    <path
      fill-rule="evenodd"
      clip-rule="evenodd"
      d="M1 1.5C1 0.671573 1.67157 0 2.5 0H10.7071L14 3.29289V13.5C14 14.3284 13.3284 15 12.5 15H2.5C1.67157 15 1 14.3284 1 13.5V1.5ZM2 6H3.5C4.32843 6 5 6.67157 5 7.5C5 8.32843 4.32843 9 3.5 9H3V11H2V6ZM10 6H13V7H11V10H12V8.5H13V11H10V6ZM7 8.61811V11H6V6H7V6.38204L8 8.38204V6H9V11H8V10.6181L7 8.61811Z"
      fill={color}
    />
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
