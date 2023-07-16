<script lang="ts">
  export let size: string = '15';
  export let role: string = 'img';
  export let color: string = 'currentColor';
  export let variation: 'solid' | 'outline' = 'outline';
  export let ariaLabel = 'kanban';
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
      d="M0.5 3.5V3C0.223858 3 0 3.22386 0 3.5H0.5ZM6.5 3.5H7C7 3.22386 6.77614 3 6.5 3V3.5ZM6.5 14.5V15C6.77614 15 7 14.7761 7 14.5H6.5ZM0.5 14.5H0C0 14.7761 0.223858 15 0.5 15V14.5ZM8.5 3.5V3C8.22386 3 8 3.22386 8 3.5H8.5ZM14.5 3.5H15C15 3.22386 14.7761 3 14.5 3V3.5ZM14.5 9.5V10C14.7761 10 15 9.77614 15 9.5H14.5ZM8.5 9.5H8C8 9.77614 8.22386 10 8.5 10V9.5ZM0 1H7V0H0V1ZM8 1H15V0H8V1ZM0.5 4H6.5V3H0.5V4ZM6 3.5V14.5H7V3.5H6ZM6.5 14H0.5V15H6.5V14ZM1 14.5V3.5H0V14.5H1ZM8.5 4H14.5V3H8.5V4ZM14 3.5V9.5H15V3.5H14ZM14.5 9H8.5V10H14.5V9ZM9 9.5V3.5H8V9.5H9Z"
      fill={color}
    />
  {:else}
    <path d="M0 1H7V0H0V1Z" fill={color} /> <path d="M8 1H15V0H8V1Z" fill={color} />
    <path
      d="M0.5 3C0.223858 3 0 3.22386 0 3.5V14.5C0 14.7761 0.223858 15 0.5 15H6.5C6.77614 15 7 14.7761 7 14.5V3.5C7 3.22386 6.77614 3 6.5 3H0.5Z"
      fill={color}
    />
    <path
      d="M8.5 3C8.22386 3 8 3.22386 8 3.5V9.5C8 9.77614 8.22386 10 8.5 10H14.5C14.7761 10 15 9.77614 15 9.5V3.5C15 3.22386 14.7761 3 14.5 3H8.5Z"
      fill={color}
    />
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
