<script lang="ts">
  export let size: string = '15';
  export let role: string = 'img';
  export let color: string = 'currentColor';
  export let variation: 'solid' | 'outline' = 'outline';
  export let ariaLabel = 'pin';
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
      fill-rule="evenodd"
      clip-rule="evenodd"
      d="M7.5 8.49478C8.604 8.49478 9.5 7.59934 9.5 6.49606C9.5 5.39278 8.604 4.49738 7.5 4.49738C6.396 4.49738 5.5 5.39278 5.5 6.49606C5.5 7.59934 6.396 8.49478 7.5 8.49478Z"
      stroke={color}
      stroke-linecap="square"
    />
    <path
      fill-rule="evenodd"
      clip-rule="evenodd"
      d="M13.5 6.49606C13.5 11.4928 8.5 14.4909 7.5 14.4909C6.5 14.4909 1.5 11.4928 1.5 6.49606C1.5 3.18522 4.187 0.5 7.5 0.5C10.813 0.5 13.5 3.18522 13.5 6.49606Z"
      stroke={color}
      stroke-linecap="square"
    />
  {:else}
    <path
      d="M6 6.49606C6 5.66924 6.67183 4.99738 7.5 4.99738C8.32817 4.99738 9 5.66924 9 6.49606C9 7.3229 8.32816 7.99478 7.5 7.99478C6.67184 7.99478 6 7.3229 6 6.49606Z"
      fill={color}
    />
    <path
      fill-rule="evenodd"
      clip-rule="evenodd"
      d="M1 6.49606C1 2.90877 3.91117 0 7.5 0C11.0888 0 14 2.90877 14 6.49606C14 9.1701 12.6617 11.2886 11.2284 12.7209C10.5102 13.4387 9.75773 13.9953 9.11325 14.3751C8.79117 14.5649 8.49017 14.7141 8.22849 14.8174C7.98144 14.9149 7.72211 14.9909 7.5 14.9909C7.27789 14.9909 7.01856 14.9149 6.77151 14.8174C6.50983 14.7141 6.20883 14.5649 5.88675 14.3751C5.24227 13.9953 4.48984 13.4387 3.77156 12.7209C2.33829 11.2886 1 9.1701 1 6.49606ZM7.5 3.99738C6.12017 3.99738 5 5.11633 5 6.49606C5 7.87579 6.12016 8.99478 7.5 8.99478C8.87984 8.99478 10 7.87579 10 6.49606C10 5.11633 8.87983 3.99738 7.5 3.99738Z"
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
@prop export let ariaLabel = 'pin';
-->
