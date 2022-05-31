<script lang="ts">
  export let size = "15";
  export let ariaLabel = "360";
  export let variation: "solid" | "outline" = "outline";
  let svgpath: string;
  let svgoutline = `<path d="M0 13.5H15M1.5 2.5L1.5 10.5C1.5 11.0523 1.94771 11.5 2.5 11.5H12.5C13.0523 11.5 13.5 11.0523 13.5 10.5V2.5C13.5 1.94772 13.0523 1.5 12.5 1.5L2.5 1.5C1.94772 1.5 1.5 1.94772 1.5 2.5Z" stroke="black"/> `;
  let svgsolid = `<path d="M2.5 1C1.67157 1 1 1.67157 1 2.5L1 10.5C1 11.3284 1.67157 12 2.5 12H12.5C13.3284 12 14 11.3284 14 10.5V2.5C14 1.67157 13.3284 1 12.5 1H2.5Z" fill="black"/> <path d="M0 14H15V13H0V14Z" fill="black"/> `;
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
