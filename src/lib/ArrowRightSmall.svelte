<script lang="ts">
  export let size: string = "15";
  export let color: string = "black" 
  export let variation: "solid" | "outline" = "outline";
  let svgpath: string;
  let svgoutline = `<path d="M8.14645 9.14645L7.79289 9.5L8.5 10.2071L8.85355 9.85355L8.14645 9.14645ZM10.5 7.5L10.8536 7.85355L11.2071 7.5L10.8536 7.14645L10.5 7.5ZM8.85355 5.14645L8.5 4.79289L7.79289 5.5L8.14645 5.85355L8.85355 5.14645ZM8.85355 9.85355L10.8536 7.85355L10.1464 7.14645L8.14645 9.14645L8.85355 9.85355ZM10.8536 7.14645L8.85355 5.14645L8.14645 5.85355L10.1464 7.85355L10.8536 7.14645ZM10.5 7H4V8H10.5V7Z" fill="${color}"/> `;
  let svgsolid = `<path fill-rule="evenodd" clip-rule="evenodd" d="M8.5 4.79291L11.2071 7.50001L8.5 10.2071L7.79289 9.50001L9.29289 8.00001H4V7.00001H9.29289L7.79289 5.50001L8.5 4.79291Z" fill="${color}"/> `;
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
export let ariaLabel="arrow right small" </script>

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
