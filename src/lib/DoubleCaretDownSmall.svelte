<script lang="ts">
  export let size = "15";
  export let ariaLabel = "360";
  export let variation: "solid" | "outline" = "outline";
  let svgpath: string;
  let svgoutline = `<path d="M9.5 8.5L7.5 10.5L5.5 8.5M9.5 5.5L7.5 7.5L5.5 5.5" stroke="black" stroke-linecap="square"/> `;
  let svgsolid = `<path fill-rule="evenodd" clip-rule="evenodd" d="M5.50001 4.79291L7.50001 6.79291L9.50001 4.79291L10.2071 5.50001L7.50001 8.20712L4.79291 5.50001L5.50001 4.79291ZM5.50001 7.79291L7.50001 9.79291L9.50001 7.79291L10.2071 8.50001L7.50001 11.2071L4.79291 8.50001L5.50001 7.79291Z" fill="black"/> `;
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
