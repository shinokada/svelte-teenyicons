<script lang="ts">
  import type { ComponentType } from 'svelte';
  export let icon: ComponentType;
  export let size: number = 15;
  export let role: string = 'img';
  export let color: string = 'currentColor';
  export let variation: 'solid' | 'outline' = 'outline';
  export let ariaLabel = 'Icon';
</script>

<svelte:component
  this={icon}
  {...$$restProps}
  {role}
  {size}
  {color}
  {variation}
  class={$$props.class}
  {ariaLabel}
/>

<!--
@component
[Go to docs](https://svelte-teenyicons.vercel.app/)
## Props
@prop export let icon: ComponentType;
@prop export let size: number = 15;
@prop export let role: string = 'img';
@prop export let color: string = 'currentColor';
@prop export let variation: 'solid' | 'outline' = 'outline';
@prop export let ariaLabel = 'Icon';
-->
