<script lang="ts">
  export let size: string = '15';
  export let role: string = 'img';
  export let color: string = 'currentColor';
  export let variation: 'solid' | 'outline' = 'outline';
  export let ariaLabel = 'globe';
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
      d="M7.5 15V12M4 14.5H11M11.4687 1C12.7144 2.09942 13.5 3.70796 13.5 5.5C13.5 8.81371 10.8137 11.5 7.5 11.5C5.96329 11.5 4.56151 10.9223 3.5 9.97221M7.5 2.5C5.84315 2.5 4.5 3.84315 4.5 5.5C4.5 7.15685 5.84315 8.5 7.5 8.5C9.15685 8.5 10.5 7.15685 10.5 5.5C10.5 3.84315 9.15685 2.5 7.5 2.5Z"
      stroke={color}
    />
  {:else}
    <path
      d="M14 5.49999C14 3.55855 13.1482 1.81543 11.7996 0.625122L11.1378 1.37486C12.2805 2.38339 13 3.85736 13 5.49999C13 8.53756 10.5375 11 7.49996 11C6.09099 11 4.8068 10.4708 3.83342 9.59964L3.1665 10.3448C4.19995 11.2697 5.53216 11.8693 6.99996 11.981V14H3.99996V15H11V14H7.99996V11.981C11.3562 11.7257 14 8.92161 14 5.49999Z"
      fill={color}
    />
    <path
      d="M7.49996 1.99999C5.56696 1.99999 3.99996 3.56699 3.99996 5.49999C3.99996 7.43299 5.56696 8.99999 7.49996 8.99999C9.43296 8.99999 11 7.43299 11 5.49999C11 3.56699 9.43296 1.99999 7.49996 1.99999Z"
      fill={color}
    />
  {/if}
</svg>

<!--
@component
[Go to docs](https://svelte-teenyicons.vercel.app/)
## Props
@prop export let size: string = '15';
@prop export let role: string = 'img';
@prop export let color: string = 'currentColor';
@prop export let variation: 'solid' | 'outline' = 'outline';
@prop export let ariaLabel = 'globe';
-->
