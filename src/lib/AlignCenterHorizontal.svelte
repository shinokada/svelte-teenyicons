<script lang="ts">
  export let size: string = "15";
  export let color: string = "black" 
  export let variation: "solid" | "outline" = "outline";
  let svgpath: string;
  let svgoutline = `<path d="M7.5 0V3.5M7.5 11.5V15M7.5 6.5V8.5M4 3.5V6.5H11V3.5H4ZM1.5 8.5V11.5H13.5V8.5H1.5Z" stroke="${color}"/> `;
  let svgsolid = `<path d="M7 0V3H3.5V7H7V8H1V12H7V15H8V12H14V8H8V7H11.5V3H8V0H7Z" fill="${color}"/> `;
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
export let ariaLabel="align center horizontal" </script>

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
