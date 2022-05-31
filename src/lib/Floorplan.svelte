<script lang="ts">
  export let size = "15";
  export let ariaLabel = "360";
  export let variation: "solid" | "outline" = "outline";
  let svgpath: string;
  let svgoutline = `<path d="M10 0.5H14.5V14.5H0.5V0.5H4.5L7.5 2.5M6.5 14.5V7.5M4 7.5H9M12 7.5H14.5" stroke="black"/> `;
  let svgsolid = `<path fill-rule="evenodd" clip-rule="evenodd" d="M0 0H4.65139L7.77735 2.08397L7.22265 2.91603L4.34861 1H1V14H6V8H4V7H9V8H7V14H14V8H12V7H14V1H10V0H15V15H0V0Z" fill="black"/> `;
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
