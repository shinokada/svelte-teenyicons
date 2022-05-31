<script lang="ts">
  export let size = "15";
  export let ariaLabel = "360";
  export let variation: "solid" | "outline" = "outline";
  let svgpath: string;
  let svgoutline = `<path d="M6 11.5H9M2.5 14.5H12.5C13.0523 14.5 13.5 14.0523 13.5 13.5V1.5C13.5 0.947715 13.0523 0.5 12.5 0.5H2.5C1.94772 0.5 1.5 0.947716 1.5 1.5V13.5C1.5 14.0523 1.94772 14.5 2.5 14.5Z" stroke="black"/> `;
  let svgsolid = `<path fill-rule="evenodd" clip-rule="evenodd" d="M1 1.5C1 0.671573 1.67157 0 2.5 0H12.5C13.3284 0 14 0.671573 14 1.5V13.5C14 14.3284 13.3284 15 12.5 15H2.5C1.67157 15 1 14.3284 1 13.5V1.5ZM6 12H9V11H6V12Z" fill="black"/> `;
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
