<script lang="ts">
  interface CtxType {
    size?: string;
    role?: string;
    color?: string;
    variation?: 'solid' | 'outline';
  }

  import { getContext } from 'svelte';
  const ctx: CtxType = getContext('iconCtx') ?? {};
  export let size: string = ctx.size || '15';
  export let role: string = ctx.role || 'img';
  export let color: string = ctx.color || 'currentColor';
  export let variation: 'solid' | 'outline' = 'outline';
  export let ariaLabel = 'bulb off';
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
      d="M4.07572 6.46985L3.58075 6.39913V6.39913L4.07572 6.46985ZM4.06567 6.5402L4.56064 6.61091L4.56064 6.61091L4.06567 6.5402ZM10.9242 6.46985L10.4293 6.54056V6.54056L10.9242 6.46985ZM10.9343 6.54021L11.4293 6.46949V6.46949L10.9343 6.54021ZM9.5 12.5V13C9.77614 13 10 12.7761 10 12.5H9.5ZM5.5 12.5H5C5 12.7761 5.22386 13 5.5 13V12.5ZM4.75549 9.15291L5.15088 8.84687L4.75549 9.15291ZM10.2445 9.15289L9.8491 8.84686L10.2445 9.15289ZM6 15H9V14H6V15ZM3.58075 6.39913L3.5707 6.46949L4.56064 6.61091L4.5707 6.54056L3.58075 6.39913ZM7.49998 3C5.52977 3 3.85938 4.44872 3.58075 6.39913L4.5707 6.54056C4.77895 5.08279 6.02742 4 7.49998 4V3ZM11.4192 6.39914C11.1406 4.44873 9.4702 3 7.49998 3V4C8.97255 4 10.221 5.0828 10.4293 6.54056L11.4192 6.39914ZM11.4293 6.46949L11.4192 6.39914L10.4293 6.54056L10.4393 6.61092L11.4293 6.46949ZM10.6399 9.45893C11.2696 8.64541 11.5885 7.58397 11.4293 6.46949L10.4393 6.61092C10.5585 7.44543 10.3209 8.23729 9.8491 8.84686L10.6399 9.45893ZM9 10.9013V12.5H10V10.9013H9ZM9.5 12H5.5V13H9.5V12ZM6 12.5V10.9013H5V12.5H6ZM3.5707 6.46949C3.41148 7.58398 3.73042 8.64543 4.36009 9.45895L5.15088 8.84687C4.67907 8.2373 4.44143 7.44544 4.56064 6.61091L3.5707 6.46949ZM6 10.9013C6 10.0775 5.56209 9.37814 5.15088 8.84687L4.36009 9.45895C4.74345 9.95426 5 10.427 5 10.9013H6ZM9.8491 8.84686C9.4379 9.37813 9 10.0775 9 10.9013H10C10 10.427 10.2565 9.95423 10.6399 9.45893L9.8491 8.84686Z"
      fill={color}
    />
  {:else}
    <path
      d="M7.49989 3C5.52968 3 3.85928 4.44872 3.58065 6.39913L3.5706 6.46949C3.41139 7.58398 3.73032 8.64543 4.35999 9.45895C4.74336 9.95426 4.9999 10.427 4.9999 10.9013V12.5C4.9999 12.7761 5.22376 13 5.4999 13H9.4999C9.77605 13 9.9999 12.7761 9.9999 12.5V10.9013C9.9999 10.427 10.2564 9.95423 10.6398 9.45893C11.2695 8.64541 11.5884 7.58397 11.4292 6.46949L11.4191 6.39914C11.1405 4.44873 9.4701 3 7.49989 3Z"
      fill={color}
    /> <path d="M5.9999 15H8.9999V14H5.9999V15Z" fill={color} />
  {/if}
</svg>

<!--
@component
[Go to docs](https://svelte-teenyicons.codewithshin.com/)
## Props
@prop export let size: string = ctx.size || '15';
@prop export let role: string = ctx.role || 'img';
@prop export let color: string = ctx.color || 'currentColor';
@prop export let variation: 'solid' | 'outline' = 'outline';
@prop export let ariaLabel = 'bulb off';
-->
