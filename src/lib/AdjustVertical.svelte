<script lang="ts">
  export let size = "15";
  export let ariaLabel = "360";
  export let variation: "solid" | "outline" = "outline";
  let svgpath: string;
  let svgoutline = `<path d="M7.5 12.5V15M12.5 6.55671e-07V2.5M2.5 6.55671e-07L2.50001 6.5M2.5 8.5V15M7.5 10.5V0M12.5 4.5V15M10.5 4.5H14.5V2.5H10.5V4.5ZM5.5 12.5H9.5V10.5H5.5V12.5ZM0.5 8.5H4.5V6.5H0.5V8.5Z" stroke="black"/> `;
  let svgsolid = `<path d="M2 0L2.00001 6H0V9H2V15H3V9H5V6H3.00001L3 0H2Z" fill="black"/> <path d="M5 10H7V0H8V10H10V13H8V15H7V13H5V10Z" fill="black"/> <path d="M12 0V2H10V5H12V15H13V5H15V2H13V0H12Z" fill="black"/> `;
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
