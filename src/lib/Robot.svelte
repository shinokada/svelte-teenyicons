<script lang="ts">
  export let size: string = '15';
  export let role: string = 'img';
  export let color: string = 'black';
  export let variation: 'solid' | 'outline' = 'outline';
  export let ariaLabel = 'robot';
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
      d="M7.5 2.5C10.2614 2.5 12.5 4.73858 12.5 7.5V13.5C12.5 14.0523 12.0523 14.5 11.5 14.5H3.5C2.94772 14.5 2.5 14.0523 2.5 13.5V7.5C2.5 4.73858 4.73858 2.5 7.5 2.5ZM7.5 2.5V0M4 11.5H11M0.5 8V12M14.5 8V12M5.5 9.5C4.94772 9.5 4.5 9.05228 4.5 8.5C4.5 7.94772 4.94772 7.5 5.5 7.5C6.05228 7.5 6.5 7.94772 6.5 8.5C6.5 9.05228 6.05228 9.5 5.5 9.5ZM9.5 9.5C8.94772 9.5 8.5 9.05228 8.5 8.5C8.5 7.94772 8.94772 7.5 9.5 7.5C10.0523 7.5 10.5 7.94772 10.5 8.5C10.5 9.05228 10.0523 9.5 9.5 9.5Z"
      stroke={color}
    />
  {:else}
    <path
      d="M5 8.5C5 8.22386 5.22386 8 5.5 8C5.77614 8 6 8.22386 6 8.5C6 8.77614 5.77614 9 5.5 9C5.22386 9 5 8.77614 5 8.5Z"
      fill={color}
    />
    <path
      d="M9 8.5C9 8.22386 9.22386 8 9.5 8C9.77614 8 10 8.22386 10 8.5C10 8.77614 9.77614 9 9.5 9C9.22386 9 9 8.77614 9 8.5Z"
      fill={color}
    />
    <path
      fill-rule="evenodd"
      clip-rule="evenodd"
      d="M8 2.02242C10.8033 2.27504 13 4.63098 13 7.5V13.5C13 14.3284 12.3284 15 11.5 15H3.5C2.67157 15 2 14.3284 2 13.5V7.5C2 4.63098 4.19675 2.27504 7 2.02242V0H8V2.02242ZM5.5 7C4.67157 7 4 7.67157 4 8.5C4 9.32843 4.67157 10 5.5 10C6.32843 10 7 9.32843 7 8.5C7 7.67157 6.32843 7 5.5 7ZM9.5 7C8.67157 7 8 7.67157 8 8.5C8 9.32843 8.67157 10 9.5 10C10.3284 10 11 9.32843 11 8.5C11 7.67157 10.3284 7 9.5 7ZM11 12H4V11H11V12Z"
      fill={color}
    /> <path d="M0 8V12H1V8H0Z" fill={color} /> <path d="M15 8H14V12H15V8Z" fill={color} />
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
