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
  export let ariaLabel = 'netlify';
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
      d="M0.5 7.5L0.146447 7.14645C-0.0488155 7.34171 -0.0488155 7.65829 0.146447 7.85355L0.5 7.5ZM7.5 0.5L7.85355 0.146447C7.65829 -0.0488155 7.34171 -0.0488155 7.14645 0.146447L7.5 0.5ZM14.5 7.5L14.8536 7.85355C15.0488 7.65829 15.0488 7.34171 14.8536 7.14645L14.5 7.5ZM7.5 14.5L7.14645 14.8536C7.34171 15.0488 7.65829 15.0488 7.85355 14.8536L7.5 14.5ZM0.853553 7.85355L7.85355 0.853553L7.14645 0.146447L0.146447 7.14645L0.853553 7.85355ZM7.14645 0.853553L14.1464 7.85355L14.8536 7.14645L7.85355 0.146447L7.14645 0.853553ZM14.1464 7.14645L7.14645 14.1464L7.85355 14.8536L14.8536 7.85355L14.1464 7.14645ZM7.85355 14.1464L0.853553 7.14645L0.146447 7.85355L7.14645 14.8536L7.85355 14.1464ZM4.3143 3.96424L14.3143 7.96424L14.6857 7.03576L4.6857 3.03576L4.3143 3.96424ZM8.58021 1.72837L3.08021 10.2284L3.91979 10.7716L9.41979 2.27163L8.58021 1.72837ZM2.1 5.8L8.1 13.8L8.9 13.2L2.9 5.2L2.1 5.8ZM0.393785 7.98859L11.8938 10.4886L12.1062 9.51141L0.606215 7.01141L0.393785 7.98859ZM2.71404 9.95187L12.214 5.45187L11.786 4.54813L2.28596 9.04813L2.71404 9.95187ZM10.0061 3.42202L8.50612 12.922L9.49388 13.078L10.9939 3.57798L10.0061 3.42202Z"
      fill={color}
    />
  {:else}
    <path
      d="M7.14645 0.146447C7.34172 -0.0488155 7.6583 -0.0488155 7.85356 0.146447L8.83363 1.12651L7.01342 4.06685L4.30815 2.98475L7.14645 0.146447Z"
      fill={color}
    />
    <path
      d="M3.53884 3.75406L2.42638 4.86652L4.71994 7.7717L6.47901 4.93012L3.53884 3.75406Z"
      fill={color}
    />
    <path
      d="M1.7144 5.5785L0.146455 7.14645C0.12315 7.16975 0.102626 7.19478 0.0848846 7.22113L3.60707 7.97589L1.7144 5.5785Z"
      fill={color}
    /> <path d="M0.659968 8.36707L1.66655 9.37365L2.84238 8.83473L0.659968 8.36707Z" fill={color} />
    <path d="M2.42086 10.128L2.93996 10.6471L3.59422 9.59016L2.42086 10.128Z" fill={color} />
    <path
      d="M3.66637 11.3735L7.14645 14.8536C7.34172 15.0488 7.6583 15.0488 7.85356 14.8536L8.17746 14.5297L8.2957 13.9148L4.81919 9.51124L3.66637 11.3735Z"
      fill={color}
    /> <path d="M9.43824 13.2689L11.9259 10.7812L9.99616 10.3677L9.43824 13.2689Z" fill={color} />
    <path
      d="M12.7681 9.93897L14.549 8.15812L10.7159 6.62489L10.185 9.38545L12.7681 9.93897Z"
      fill={color}
    />
    <path
      d="M14.9209 7.22983C14.9018 7.20028 14.8794 7.1723 14.8536 7.14645L12.9906 5.28349L11.6226 5.91051L14.9209 7.22983Z"
      fill={color}
    /> <path d="M12.2363 4.52918L11.2992 3.59205L11.0109 5.0908L12.2363 4.52918Z" fill={color} />
    <path
      d="M10.4451 2.73797L9.56004 1.85293L7.9561 4.44392L9.96267 5.24655L10.4451 2.73797Z"
      fill={color}
    /> <path d="M5.9983 8.48829L9.6622 6.80901L9.20703 9.17588L5.9983 8.48829Z" fill={color} />
    <path d="M6.11237 9.53544L9.01814 10.1581L8.54526 12.6171L6.11237 9.53544Z" fill={color} />
    <path d="M6.18693 7.30181L9.08617 5.97299L7.42169 5.3072L6.18693 7.30181Z" fill={color} />
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
@prop export let ariaLabel = 'netlify';
-->
