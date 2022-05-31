<script lang="ts">
  export let size = "15";
  export let ariaLabel = "360";
  export let variation: "solid" | "outline" = "outline";
  let svgpath: string;
  let svgoutline = `<path d="M0 7.5H15M4.5 12.5H10.5M4.5 12.5C2.84315 12.5 1.5 11.1569 1.5 9.5V3.5C1.5 1.84315 2.84315 0.5 4.5 0.5H6.5V2M4.5 12.5V15M10.5 12.5C12.1569 12.5 13.5 11.1569 13.5 9.5V7.5M10.5 12.5V15M5 3.5H8" stroke="black"/> `;
  let svgsolid = `<path d="M2 3.5C2 2.11929 3.11929 1 4.5 1H6V2H7V0H4.5C2.567 0 1 1.567 1 3.5V7H0V8H1V9.5C1 11.2632 2.30385 12.7219 4 12.9646V15H5V13H10V15H11V12.9646C12.6961 12.7219 14 11.2632 14 9.5V8H15V7H2V3.5Z" fill="black"/> <path d="M8 4H5V3H8V4Z" fill="black"/> `;
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
