<script lang="ts">
  export let size: string = "15";
  export let color: string = "black" 
  export let variation: "solid" | "outline" = "outline";
  let svgpath: string;
  let svgoutline = `<path d="M0.5 0V15M3.5 3.5V6.5H10.5V3.5H3.5ZM3.5 8.5V11.5H14.5V8.5H3.5Z" stroke="${color}"/> `;
  let svgsolid = `<path d="M0 0V15H1V0H0Z" fill="${color}"/> <path d="M11 3H3V7H11V3Z" fill="${color}"/> <path d="M15 8H3V12H15V8Z" fill="${color}"/> `;
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
export let ariaLabel="align left" </script>

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
