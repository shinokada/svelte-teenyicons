<script lang="ts">
  export let size: string = "15";
  export let role: string = "img";
  export let color: string = "currentColor" 
  export let variation: "solid" | "outline" = "outline";
export let ariaLabel="send" </script>

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
    <path d="M14.5 0.5L14.9596 0.69696C15.0401 0.509038 14.9981 0.291016 14.8536 0.146447C14.709 0.00187701 14.491 -0.0401102 14.303 0.0404275L14.5 0.5ZM0.5 6.5L0.30304 6.04043C0.130457 6.11439 0.0138614 6.27881 0.00114754 6.46614C-0.0115663 6.65348 0.0817453 6.83214 0.242752 6.92875L0.5 6.5ZM8.5 14.5L8.07125 14.7572C8.16786 14.9183 8.34652 15.0116 8.53386 14.9989C8.72119 14.9861 8.88561 14.8695 8.95957 14.697L8.5 14.5ZM14.303 0.0404275L0.30304 6.04043L0.69696 6.95957L14.697 0.959573L14.303 0.0404275ZM0.242752 6.92875L5.24275 9.92875L5.75725 9.07125L0.757248 6.07125L0.242752 6.92875ZM5.07125 9.75725L8.07125 14.7572L8.92875 14.2428L5.92875 9.24275L5.07125 9.75725ZM8.95957 14.697L14.9596 0.69696L14.0404 0.30304L8.04043 14.303L8.95957 14.697ZM14.1464 0.146447L5.14645 9.14645L5.85355 9.85355L14.8536 0.853553L14.1464 0.146447Z" fill="{color}"/> 
  {:else}
    <path d="M14.9541 0.709802C14.93 0.761862 14.8965 0.810638 14.8536 0.853553L5.40076 10.3064L8.07126 14.7573C8.16786 14.9183 8.34653 15.0116 8.53386 14.9989C8.72119 14.9862 8.88561 14.8696 8.95958 14.697L14.9541 0.709802Z" fill="{color}"/> <path d="M4.69366 9.59931L0.242756 6.92876C0.0817496 6.83216 -0.0115621 6.65349 0.00115182 6.46616C0.0138657 6.27883 0.130462 6.11441 0.303045 6.04044L14.293 0.0447451C14.2399 0.0688812 14.1902 0.102782 14.1465 0.146447L4.69366 9.59931Z" fill="{color}"/> 
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