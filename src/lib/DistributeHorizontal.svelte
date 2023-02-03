<script lang="ts">
  export let size: string = "15";
  export let color: string = "black" 
  export let variation: "solid" | "outline" = "outline";
  let svgpath: string;
  let svgoutline = `<path d="M0.5 15V0M14.5 15V0M5.5 13.5V1.5H9.5V13.5H5.5Z" stroke="${color}"/> `;
  let svgsolid = `<path d="M1 15V0H0V15H1Z" fill="${color}"/> <path d="M15 15V0H14V15H15Z" fill="${color}"/> <path d="M10 1H5V14H10V1Z" fill="${color}"/> `;
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
export let ariaLabel="distribute horizontal" </script>

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
