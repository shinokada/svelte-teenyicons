<script lang="ts">
  export let size: string = "15";
  export let color: string = "black" 
  export let variation: "solid" | "outline" = "outline";
  let svgpath: string;
  let svgoutline = `<path d="M10 9L7.5 11L5 9M5 6L7.5 4L10 6" stroke="${color}" stroke-linecap="square"/> `;
  let svgsolid = `<path d="M7.50005 3.375L11.0001 6L4.00005 6L7.50005 3.375Z" fill="${color}"/> <path d="M7.50005 11.625L4.00005 9H11.0001L7.50005 11.625Z" fill="${color}"/> `;
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
export let ariaLabel="caret vertical small" </script>

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
