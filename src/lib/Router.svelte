<script lang="ts">
  export let size: string = "15";
  export let role: string = "img";
  export let color: string = "currentColor" 
  export let variation: "solid" | "outline" = "outline";
export let ariaLabel="router" </script>

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
    <path d="M1.5 9.5V9H1V9.5H1.5ZM13.5 9.5H14V9H13.5V9.5ZM13.5 14.5V15H14V14.5H13.5ZM1.5 14.5H1V15H1.5V14.5ZM3.21907 6.16133C4.37371 4.76169 5.91677 4 7.50004 4V3C5.58263 3 3.76839 3.92402 2.44768 5.52496L3.21907 6.16133ZM7.50004 4C9.08331 4 10.6264 4.76169 11.781 6.16133L12.5524 5.52496C11.2317 3.92402 9.41745 3 7.50004 3V4ZM0.885695 4.31818C2.65795 2.16988 5.03983 1 7.5 1V0C4.70916 0 2.05508 1.32925 0.114305 3.68182L0.885695 4.31818ZM7.5 1C9.96017 1 12.342 2.16988 14.1143 4.31818L14.8857 3.68182C12.9449 1.32925 10.2908 0 7.5 0V1ZM7 6V9H8V6H7ZM1.5 10H13.5V9H1.5V10ZM13 9.5V14.5H14V9.5H13ZM13.5 14H1.5V15H13.5V14ZM2 14.5V9.5H1V14.5H2Z" fill="{color}"/> 
  {:else}
    <path fill-rule="evenodd" clip-rule="evenodd" d="M7.5 1C5.03982 1 2.65795 2.16988 0.885693 4.31818L0.114304 3.68182C2.05507 1.32925 4.70915 0 7.5 0C10.2908 0 12.9449 1.32925 14.8857 3.68182L14.1143 4.31818C12.342 2.16988 9.96017 1 7.5 1ZM7.50004 4C5.91677 4 4.37371 4.76169 3.21907 6.16133L2.44768 5.52496C3.76839 3.92402 5.58263 3 7.50004 3C9.41745 3 11.2317 3.92402 12.5524 5.52496L11.781 6.16133C10.6264 4.76169 9.08331 4 7.50004 4ZM7 9V6H8V9H14V15H0.999998V9H7Z" fill="{color}"/> 
  {/if}
</svg>
