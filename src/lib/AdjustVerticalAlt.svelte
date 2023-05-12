<script lang="ts">
  export let size: string = "15";
  export let color: string = "black" 
  export let variation: "solid" | "outline" = "outline";
  let svgpath: string;
  let svgoutline = `<path d="M3.5 0L3.5 8.5M3.5 8.5C2.39543 8.5 1.5 9.39543 1.5 10.5C1.5 11.6046 2.39543 12.5 3.5 12.5M3.5 8.5C4.60457 8.5 5.5 9.39543 5.5 10.5C5.5 11.6046 4.60457 12.5 3.5 12.5M3.5 12.5V15M11.5 0L11.5 2.5M11.5 2.5C10.3954 2.5 9.5 3.39543 9.5 4.5C9.5 5.60457 10.3954 6.5 11.5 6.5M11.5 2.5C12.6046 2.5 13.5 3.39543 13.5 4.5C13.5 5.60457 12.6046 6.5 11.5 6.5M11.5 6.5V15" stroke="${color}"/> `;
  let svgsolid = `<path d="M3 0L3 8.05001C1.85888 8.28164 1 9.29052 1 10.5C1 11.7095 1.85888 12.7184 3 12.95V15H4V12.95C5.14112 12.7184 6 11.7095 6 10.5C6 9.29052 5.14112 8.28164 4 8.05001L4 0H3Z" fill="${color}"/> <path d="M11 0L11 2.05001C9.85888 2.28164 9 3.29052 9 4.5C9 5.70948 9.85888 6.71836 11 6.94999V15H12V6.94999C13.1411 6.71836 14 5.70948 14 4.5C14 3.29052 13.1411 2.28164 12 2.05001L12 0H11Z" fill="${color}"/> `;
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
export let ariaLabel="adjust vertical alt" </script>

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
