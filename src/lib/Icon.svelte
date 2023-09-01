<script lang="ts">
  import type { ComponentType } from 'svelte';
  export let icon: ComponentType;
  export let size: number = 15;
  export let role: string = 'img';
  export let color: string = 'currentColor';
  export let variation: "solid" | "outline" = "outline";
  export let ariaLabel = 'Icon';
</script>

<svelte:component 
  {...$$restProps} 
  {role}
  this={icon} 
  {size}
  {color}
  {variation}
  class={$$props.class} 
  {ariaLabel}
/>