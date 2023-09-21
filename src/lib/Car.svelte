<script lang="ts">
  export let size: string = '15';
  export let role: string = 'img';
  export let color: string = 'currentColor';
  export let variation: 'solid' | 'outline' = 'outline';
  export let ariaLabel = 'car';
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
      d="M14.5 6.4967H15V6.35813L14.9287 6.23933L14.5 6.4967ZM0.5 6.4967L0.0713284 6.23933L0 6.35813V6.4967H0.5ZM2.62597 2.95576L2.19729 2.69839L2.62597 2.95576ZM12.374 2.95576L12.8027 2.69839L12.374 2.95576ZM3.5 11.5V11H3V11.5H3.5ZM11.5 11.5H12V11H11.5V11.5ZM14 6.4967V12.5H15V6.4967H14ZM0.928672 6.75408L3.05464 3.21314L2.19729 2.69839L0.0713284 6.23933L0.928672 6.75408ZM5.19799 2H9.80201V1H5.19799V2ZM11.9454 3.21314L14.0713 6.75408L14.9287 6.23933L12.8027 2.69839L11.9454 3.21314ZM2.5 13H1.5V14H2.5V13ZM3 11.5V12.5H4V11.5H3ZM13.5 13H12.5V14H13.5V13ZM12 12.5V11.5H11V12.5H12ZM11.5 11H3.5V12H11.5V11ZM1 12.5V6.4967H0V12.5H1ZM12.5 13C12.2239 13 12 12.7761 12 12.5H11C11 13.3284 11.6716 14 12.5 14V13ZM2.5 14C3.32843 14 4 13.3284 4 12.5H3C3 12.7761 2.77614 13 2.5 13V14ZM1.5 13C1.22386 13 1 12.7761 1 12.5H0C0 13.3284 0.671573 14 1.5 14V13ZM9.80201 2C10.6799 2 11.4935 2.46048 11.9454 3.21314L12.8027 2.69839C12.1701 1.64467 11.0311 1 9.80201 1V2ZM3.05464 3.21314C3.50653 2.46048 4.3201 2 5.19799 2V1C3.96894 1 2.82994 1.64467 2.19729 2.69839L3.05464 3.21314ZM14 12.5C14 12.7761 13.7761 13 13.5 13V14C14.3284 14 15 13.3284 15 12.5H14ZM2 10H5V9H2V10ZM13 9H10V10H13V9ZM3 7H12V6H3V7Z"
      fill={color}
    />
  {:else}
    <path
      fill-rule="evenodd"
      clip-rule="evenodd"
      d="M2.19729 2.69839C2.82994 1.64467 3.96894 1 5.19799 1H9.80201C11.0311 1 12.1701 1.64467 12.8027 2.69839L15 6.35813V12.5C15 13.3284 14.3284 14 13.5 14H12.5C11.6716 14 11 13.3284 11 12.5V12H4V12.5C4 13.3284 3.32843 14 2.5 14H1.5C0.671573 14 0 13.3284 0 12.5V6.35813L2.19729 2.69839ZM12 7H3V6H12V7ZM2 10H5V9H2V10ZM13 9H10V10H13V9Z"
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
@prop export let ariaLabel = 'car';
-->
