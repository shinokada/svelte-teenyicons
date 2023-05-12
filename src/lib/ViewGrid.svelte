<script lang="ts">
  export let size: string = "15";
  export let color: string = "black" 
  export let variation: "solid" | "outline" = "outline";
  let svgpath: string;
  let svgoutline = `<path d="M0 5.5H15M0 1.5H15M0 9.5H15M0 13.5H15M9.5 7.98702e-06L9.5 15M13.5 8.10623e-06L13.5 15M5.5 7.7486e-06L5.5 15M1.5 7.62939e-06L1.5 15" stroke="${color}"/> `;
  let svgsolid = `<path fill-rule="evenodd" clip-rule="evenodd" d="M0.999997 1L0.999997 7.62939e-06H2V1H5V7.62939e-06H6V1H9V7.62939e-06H10V1H13V7.62939e-06H14V1H15V2H14V5H15V6H14L14 9H15V10H14V13H15V14H14V15H13V14H10V15H9V14H6V15H5V14H2V15H0.999996L0.999996 14H0V13H0.999996L0.999996 10H0V9H0.999996L0.999997 6H0V5H0.999997L0.999997 2H0V1H0.999997ZM2 2L2 5H5V2H2ZM6 2V5H9V2H6ZM10 2V5H13V2H10ZM13 6H10L10 9H13L13 6ZM13 10H10V13H13V10ZM9 13V10H6V13H9ZM5 13V10H2L2 13H5ZM2 9H5L5 6H2L2 9ZM6 6L6 9H9L9 6H6Z" fill="${color}"/> `;
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
export let ariaLabel="view grid" </script>

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
