<script lang="ts">
  export let size: string = "15";
  export let color: string = "black" 
  export let variation: "solid" | "outline" = "outline";
  let svgpath: string;
  let svgoutline = `<path d="M1.5 1.5V1C1.22386 1 1 1.22386 1 1.5H1.5ZM1.5 2H6.99999V1H1.5V2ZM1 1.5V7H2V1.5H1ZM1.14645 1.85355L13.1464 13.8536L13.8535 13.1464L1.85355 1.14645L1.14645 1.85355Z" fill="${color}"/> `;
  let svgsolid = `<path fill-rule="evenodd" clip-rule="evenodd" d="M1.00001 1H7V2H2.70711L13.8536 13.1464L13.1464 13.8536L2.00001 2.70711V7H1.00001V1Z" fill="${color}"/> `;
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
export let ariaLabel="top left" </script>

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
