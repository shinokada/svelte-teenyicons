<script lang="ts">
  export let size: string = "15";
  export let role: string = "img";
  export let color: string = "currentColor" 
  export let variation: "solid" | "outline" = "outline";
export let ariaLabel="flag" </script>

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
    <path d="M14.5 0.5L14.9569 0.703069C15.0256 0.548403 15.0115 0.369461 14.9192 0.227543C14.827 0.0856253 14.6693 0 14.5 0V0.5ZM0.5 0.5V0C0.223858 0 0 0.223858 0 0.5L0.5 0.5ZM14.5 9.5V10C14.6693 10 14.827 9.91437 14.9192 9.77246C15.0115 9.63054 15.0256 9.4516 14.9569 9.29693L14.5 9.5ZM12.5 5L12.0431 4.79693C11.9856 4.92621 11.9856 5.07379 12.0431 5.20307L12.5 5ZM14.5 0H0.5V1H14.5V0ZM0 0.5V9.5H1V0.5H0ZM0.5 10H14.5V9H0.5V10ZM14.9569 9.29693L12.9569 4.79693L12.0431 5.20307L14.0431 9.70307L14.9569 9.29693ZM12.9569 5.20307L14.9569 0.703069L14.0431 0.296931L12.0431 4.79693L12.9569 5.20307ZM1 15V9.5H0V15H1Z" fill="{color}"/> 
  {:else}
    <path d="M0 0.5C0 0.223858 0.223858 0 0.5 0H14.5C14.6693 0 14.827 0.0856253 14.9192 0.227543C15.0115 0.369461 15.0256 0.548403 14.9569 0.703069L13.0472 5L14.9569 9.29693C15.0256 9.4516 15.0115 9.63054 14.9192 9.77246C14.827 9.91437 14.6693 10 14.5 10H1V15H0V0.5Z" fill="{color}"/> 
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