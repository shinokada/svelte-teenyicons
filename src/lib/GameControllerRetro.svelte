<script lang="ts">
  export let size = "15";
  export let ariaLabel = "360";
  export let variation: "solid" | "outline" = "outline";
  let svgpath: string;
  let svgoutline = `<path d="M8 5.5H10M4.5 6V9M3 7.5H6M10 9.5H12M0.5 3.5L0.5 11.5C0.5 12.0523 0.947716 12.5 1.5 12.5L13.5 12.5C14.0523 12.5 14.5 12.0523 14.5 11.5V3.5C14.5 2.94772 14.0523 2.5 13.5 2.5L1.5 2.5C0.947716 2.5 0.5 2.94772 0.5 3.5Z" stroke="black"/> `;
  let svgsolid = `<path fill-rule="evenodd" clip-rule="evenodd" d="M13.5 2C14.3284 2 15 2.67157 15 3.5V11.5C15 12.3284 14.3284 13 13.5 13L1.5 13C0.671573 13 0 12.3284 0 11.5V3.5C0 2.67157 0.671573 2 1.5 2H13.5ZM10 6H8V5H10V6ZM4 7V6H5V7H6V8H5V9H4V8H3V7H4ZM12 10H10V9H12V10Z" fill="black"/> `;
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
>
  {@html svgpath}
</svg>
