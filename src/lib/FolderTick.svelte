<script lang="ts">
  export let size: string = "15";
  export let color: string = "black" 
  export let variation: "solid" | "outline" = "outline";
  let svgpath: string;
  let svgoutline = `<path d="M5 8.5L7 10.5L10.5 6.5M0.5 2.5V12.5C0.5 13.0523 0.947715 13.5 1.5 13.5H13.5C14.0523 13.5 14.5 13.0523 14.5 12.5V4.5C14.5 3.94772 14.0523 3.5 13.5 3.5H7.5L5.5 1.5H1.5C0.947715 1.5 0.5 1.94772 0.5 2.5Z" stroke="${color}"/> `;
  let svgsolid = `<path fill-rule="evenodd" clip-rule="evenodd" d="M0 2.5C0 1.67157 0.671573 1 1.5 1H5.70711L7.70711 3H13.5C14.3284 3 15 3.67157 15 4.5V12.5C15 13.3284 14.3284 14 13.5 14H1.5C0.671573 14 0 13.3284 0 12.5V2.5ZM7.02439 11.2315L10.8763 6.82928L10.1237 6.17078L6.97568 9.76857L5.35359 8.14648L4.64648 8.85358L7.02439 11.2315Z" fill="${color}"/> `;
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
export let ariaLabel="folder tick" </script>

<svg
  xmlns="http://www.w3.org/2000/svg"
  width={size}
  height={size}
  fill="none"
  class={$$props.class}
  {...$$restProps}
  aria-label={ariaLabel}
  viewBox="0 0 15 15"
  on:click 
  on:mouseenter 
  on:mouseleave 
  on:mouseover 
  on:mouseout 
  on:blur 
  on:focus 
>
  {@html svgpath}
</svg>
