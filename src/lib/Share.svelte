<script lang="ts">
  export let size: string = '15';
  export let color: string = 'black';
  export let variation: 'solid' | 'outline' = 'outline';
  export let ariaLabel = 'share';
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
      d="M4.5 7.5L8.5 7.5M11 4L8.5 7.49542L11 11M14.5 2.4987C14.5 3.60198 13.604 4.49739 12.5 4.49739C11.396 4.49739 10.5 3.60198 10.5 2.4987C10.5 1.39542 11.396 0.5 12.5 0.5C13.604 0.5 14.5 1.39542 14.5 2.4987ZM14.5 12.4922C14.5 13.5954 13.604 14.4909 12.5 14.4909C11.396 14.4909 10.5 13.5954 10.5 12.4922C10.5 11.3889 11.396 10.4935 12.5 10.4935C13.604 10.4935 14.5 11.3889 14.5 12.4922ZM4.5 7.49543C4.5 8.59871 3.604 9.49413 2.5 9.49413C1.396 9.49413 0.5 8.59871 0.5 7.49543C0.5 6.39215 1.396 5.49673 2.5 5.49673C3.604 5.49673 4.5 6.39215 4.5 7.49543Z"
      stroke={color}
      stroke-linecap="square"
    />
  {:else}
    <path
      d="M10 2.4987C10 1.11897 11.1202 0 12.5 0C13.8798 0 15 1.11897 15 2.4987C15 3.87843 13.8798 4.99739 12.5 4.99739C12.119 4.99739 11.7578 4.91209 11.4345 4.75954L9.13117 7.51937L11.1694 10.3767C11.5549 10.1339 12.0111 9.99347 12.5 9.99347C13.8798 9.99347 15 11.1124 15 12.4922C15 13.8719 13.8798 14.9909 12.5 14.9909C11.1202 14.9909 10 13.8719 10 12.4922C10 11.9665 10.1626 11.4788 10.4401 11.0763L8.24567 8H4.94895C4.71527 9.13796 3.70698 9.99413 2.5 9.99413C1.12017 9.99413 0 8.87516 0 7.49543C0 6.1157 1.12017 4.99673 2.5 4.99673C3.71021 4.99673 4.72066 5.85749 4.95081 7L8.26212 7L10.6327 4.15968C10.2392 3.71816 10 3.13627 10 2.4987Z"
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
