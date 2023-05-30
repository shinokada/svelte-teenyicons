<script lang="ts">
  export let size: string = '15';
  export let color: string = 'black';
  export let variation: 'solid' | 'outline' = 'outline';
  export let ariaLabel = 'google play store';
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
      d="M1.5 0.5L1.75194 0.0681106C1.59729 -0.0220988 1.40622 -0.0227402 1.25097 0.0664289C1.09572 0.155598 1 0.320967 1 0.5H1.5ZM1.5 14.5H1C1 14.679 1.09572 14.8444 1.25097 14.9336C1.40622 15.0227 1.59729 15.0221 1.75194 14.9319L1.5 14.5ZM13.5 7.5L13.7519 7.93189C13.9055 7.84228 14 7.67783 14 7.5C14 7.32217 13.9055 7.15772 13.7519 7.06811L13.5 7.5ZM1 0.5V14.5H2V0.5H1ZM1.75194 14.9319L13.7519 7.93189L13.2481 7.06811L1.24806 14.0681L1.75194 14.9319ZM13.7519 7.06811L1.75194 0.0681106L1.24806 0.931889L13.2481 7.93189L13.7519 7.06811ZM1.82925 12.8763L9.82925 5.87629L9.17075 5.12371L1.17075 12.1237L1.82925 12.8763ZM1.17075 2.87629L9.17075 9.87629L9.82925 9.12371L1.82925 2.12371L1.17075 2.87629Z"
      fill={color}
    />
  {:else}
    <path
      d="M1.25097 0.0664289C1.40622 -0.0227402 1.59729 -0.0220988 1.75194 0.0681106L9.59402 4.64266L7.16668 6.82726L1 1.27725V0.5C1 0.320967 1.09572 0.155598 1.25097 0.0664289Z"
      fill={color}
    /> <path d="M1 2.62262V12.3773L6.41925 7.49994L1 2.62262Z" fill={color} />
    <path
      d="M1 13.7226V14.5C1 14.679 1.09572 14.8444 1.25097 14.9336C1.40622 15.0227 1.59729 15.0221 1.75194 14.9319L9.59409 10.3573L7.16668 8.17262L1 13.7226Z"
      fill={color}
    />
    <path
      d="M10.5011 9.82822L13.7519 7.93189C13.9055 7.84228 14 7.67783 14 7.5C14 7.32217 13.9055 7.15772 13.7519 7.06811L10.501 5.17173L7.9141 7.49994L10.5011 9.82822Z"
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
