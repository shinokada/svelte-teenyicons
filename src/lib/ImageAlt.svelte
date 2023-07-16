<script lang="ts">
  export let size: string = '15';
  export let role: string = 'img';
  export let color: string = 'currentColor';
  export let variation: 'solid' | 'outline' = 'outline';
  export let ariaLabel = 'image alt';
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
      d="M10 3.5H11M14.5 9.49347L11.5 6.49543L8.5 9.49347L4.5 4.49673L0.5 9.49999M1.5 0.5H13.5C14.0523 0.5 14.5 0.947715 14.5 1.5V13.5C14.5 14.0523 14.0523 14.5 13.5 14.5H1.5C0.947716 14.5 0.5 14.0523 0.5 13.5V1.5C0.5 0.947716 0.947715 0.5 1.5 0.5Z"
      stroke={color}
    />
  {:else}
    <path d="M11 4H10V3H11V4Z" fill={color} />
    <path
      fill-rule="evenodd"
      clip-rule="evenodd"
      d="M0 1.5C0 0.671573 0.671573 0 1.5 0H13.5C14.3284 0 15 0.671573 15 1.5V13.5C15 13.5032 15 13.5065 15 13.5097C14.9948 14.3337 14.3252 15 13.5 15H1.5C0.885073 15 0.35657 14.63 0.125003 14.1004C0.112847 14.0726 0.101509 14.0444 0.0910197 14.0157C0.0806793 13.9875 0.0711637 13.9589 0.0625022 13.9299C0.0226903 13.7965 0.000921331 13.6554 2.8604e-05 13.5094C9.54385e-06 13.5062 0 13.5031 0 13.5V1.5ZM14 8.28693L11.5 5.78856L8.54145 8.74518L4.49975 3.69635L1 8.07388V1.5C1 1.22386 1.22386 1 1.5 1H13.5C13.7761 1 14 1.22386 14 1.5V8.28693Z"
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
