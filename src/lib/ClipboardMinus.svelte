<script lang="ts">
  export let size = "15";
  export let ariaLabel = "360";
  export let variation: "solid" | "outline" = "outline";
  let svgpath: string;
  let svgoutline = `<path d="M11 1.5H13.5V13.5C13.5 14.0523 13.0523 14.5 12.5 14.5H2.5C1.94772 14.5 1.5 14.0523 1.5 13.5V1.5H4M5 8.5H10M4.5 0.5H10.5V2.5C10.5 3.05228 10.0523 3.5 9.5 3.5H5.5C4.94772 3.5 4.5 3.05228 4.5 2.5V0.5Z" stroke="black"/> `;
  let svgsolid = `<path fill-rule="evenodd" clip-rule="evenodd" d="M4 0H11V1H14V13.5C14 14.3284 13.3284 15 12.5 15H2.5C1.67157 15 1 14.3284 1 13.5V1H4V0ZM5 1H10V2.5C10 2.77614 9.77614 3 9.5 3H5.5C5.22386 3 5 2.77614 5 2.5V1ZM5 9H10V8H5V9Z" fill="black"/> `;
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
