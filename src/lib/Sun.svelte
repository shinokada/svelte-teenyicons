<script lang="ts">
  export let size: string = '15';
  export let color: string = 'black';
  export let variation: 'solid' | 'outline' = 'outline';
  export let ariaLabel = 'sun';
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
      d="M7.5 1.49933V0.5M7.5 14.4908V13.4915M13.5 7.49542H14.5M1.5 7.49542H0.5M2.5 2.49866L1.5 1.49933M13.5 1.49933L12.5 2.49866M2.5 12.4921L1.5 13.4915M13.5 13.4915L12.5 12.4921M10.5 7.49542C10.5 9.15134 9.157 10.4935 7.5 10.4935C5.843 10.4935 4.5 9.15134 4.5 7.49542C4.5 5.8395 5.843 4.49738 7.5 4.49738C9.157 4.49738 10.5 5.8395 10.5 7.49542Z"
      stroke={color}
      stroke-linecap="square"
    />
  {:else}
    <path d="M8 1.99933V0H7V1.99933H8Z" fill={color} />
    <path
      d="M3.20711 2.49842L1.49976 0.792222L0.792893 1.49957L2.50024 3.20576L3.20711 2.49842Z"
      fill={color}
    />
    <path
      d="M12.4998 3.20576L14.2071 1.49957L13.5002 0.792222L11.7929 2.49842L12.4998 3.20576Z"
      fill={color}
    />
    <path
      d="M7.5 3.99738C5.56716 3.99738 4 5.56305 4 7.49542C4 9.42779 5.56716 10.9935 7.5 10.9935C9.43284 10.9935 11 9.42779 11 7.49542C11 5.56305 9.43284 3.99738 7.5 3.99738Z"
      fill={color}
    /> <path d="M2 6.99542H0V7.99542H2V6.99542Z" fill={color} />
    <path d="M15 6.99542H13V7.99542H15V6.99542Z" fill={color} />
    <path
      d="M1.49978 14.1986L3.20711 12.4923L2.50022 11.785L0.792893 13.4913L1.49978 14.1986Z"
      fill={color}
    />
    <path
      d="M14.2071 13.4913L12.4998 11.785L11.7929 12.4923L13.5002 14.1986L14.2071 13.4913Z"
      fill={color}
    /> <path d="M8 14.9908V12.9915H7V14.9908H8Z" fill={color} />
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
