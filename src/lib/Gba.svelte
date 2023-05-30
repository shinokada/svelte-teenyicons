<script lang="ts">
  export let size: string = '15';
  export let color: string = 'black';
  export let variation: 'solid' | 'outline' = 'outline';
  export let ariaLabel = 'gba';
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
      d="M1.99997 6.5H4.99997M12 6.5H13M11 8.5H12M3.49997 5V8M5.10553 2.5H9.89442C10.2893 2.5 10.6753 2.61688 11.0038 2.8359L12 3.5H12.1377C13.187 3.5 14.0579 4.3109 14.1327 5.35751L14.4523 9.83326C14.4812 10.2368 14.264 10.618 13.9021 10.7989L11.812 11.844C11.6046 11.9477 11.3865 12.0284 11.1615 12.0846C8.75748 12.6856 6.24247 12.6856 3.83844 12.0846C3.61347 12.0284 3.39533 11.9477 3.18792 11.844L1.09784 10.7989C0.735964 10.618 0.518772 10.2368 0.547598 9.83326L0.867295 5.3575C0.942053 4.31089 1.81293 3.5 2.86221 3.5H2.99997L3.99612 2.8359C4.32466 2.61688 4.71068 2.5 5.10553 2.5Z"
      stroke={color}
    />
  {:else}
    <path
      fill-rule="evenodd"
      clip-rule="evenodd"
      d="M3.7189 2.41987C4.12957 2.14609 4.61209 2 5.10565 2H9.89455C10.3881 2 10.8706 2.1461 11.2813 2.41987L12.1515 3.00004C13.457 3.00706 14.5384 4.01817 14.6315 5.32188L14.9512 9.79764C14.9944 10.403 14.6687 10.9747 14.1258 11.2461L12.0358 12.2912C11.7957 12.4112 11.5433 12.5046 11.2829 12.5697C8.79925 13.1906 6.20095 13.1906 3.7173 12.5697C3.45694 12.5046 3.20448 12.4112 2.96444 12.2912L0.874364 11.2461C0.331546 10.9747 0.00575782 10.403 0.0489969 9.79764L0.368694 5.32188C0.461816 4.01817 1.54318 3.00706 2.84866 3.00004L3.7189 2.41987ZM3 8V7H2V6H3V5H4V6H5V7H4V8H3ZM13 7H12V6H13V7ZM11 9H12V8H11V9Z"
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
