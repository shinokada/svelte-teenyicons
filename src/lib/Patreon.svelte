<script lang="ts">
  export let size: string = "15";
  export let color: string = "black" 
  export let variation: "solid" | "outline" = "outline";
  let svgpath: string;
  let svgoutline = `<path d="M2.5 0.5H0.5V14.5H2.5V0.5Z" stroke="${color}"/> <path d="M4.5 5.5C4.5 8.26142 6.73858 10.5 9.5 10.5C12.2614 10.5 14.5 8.26142 14.5 5.5C14.5 2.73858 12.2614 0.5 9.5 0.5C6.73858 0.5 4.5 2.73858 4.5 5.5Z" stroke="${color}"/> `;
  let svgsolid = `<path d="M3 0H0V15H3V0Z" fill="${color}"/> <path d="M9.5 0C6.46243 0 4 2.46243 4 5.5C4 8.53757 6.46243 11 9.5 11C12.5376 11 15 8.53757 15 5.5C15 2.46243 12.5376 0 9.5 0Z" fill="${color}"/> `;
  switch (variation) {
    case "outline":
      svgpath = svgoutline;
      break;
    case "solid":
      svgpath = svgsolid;
      break;
    default:
      svgpath = svgoutline;
  }
export let ariaLabel="patreon" </script>

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
  {@html svgpath}
</svg>
