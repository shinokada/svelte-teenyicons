<script lang="ts">
  export let size: string = "15";
  export let color: string = "black" 
  export let variation: "solid" | "outline" = "outline";
  let svgpath: string;
  let svgoutline = `<path d="M4.5 6.5V3.5C4.5 1.84315 5.84315 0.5 7.5 0.5C9.15685 0.5 10.5 1.84315 10.5 3.5V4M2.5 6.5H12.5C13.0523 6.5 13.5 6.94772 13.5 7.5V13.5C13.5 14.0523 13.0523 14.5 12.5 14.5H2.5C1.94772 14.5 1.5 14.0523 1.5 13.5V7.5C1.5 6.94772 1.94772 6.5 2.5 6.5Z" stroke="${color}"/> `;
  let svgsolid = `<path d="M5 3.5C5 2.11929 6.11929 1 7.5 1C8.88071 1 10 2.11929 10 3.5V4H11V3.5C11 1.567 9.433 0 7.5 0C5.567 0 4 1.567 4 3.5V6H2.5C1.67157 6 1 6.67157 1 7.5V13.5C1 14.3284 1.67157 15 2.5 15H12.5C13.3284 15 14 14.3284 14 13.5V7.5C14 6.67157 13.3284 6 12.5 6H5V3.5Z" fill="${color}"/> `;
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
export let ariaLabel="unlock" </script>

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
