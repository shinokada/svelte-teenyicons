<script lang="ts">
  export let size: string = "15";
  export let color: string = "black" 
  export let variation: "solid" | "outline" = "outline";
  let svgpath: string;
  let svgoutline = `<path d="M0 5.5H2M13 5.5H15M0 1.5H2M13 1.5H15M0 9.5H15M0 13.5H15M5.5 0.5H9.5C10.0523 0.5 10.5 0.947715 10.5 1.5V5.5C10.5 6.05228 10.0523 6.5 9.5 6.5H5.5C4.94772 6.5 4.5 6.05228 4.5 5.5V1.5C4.5 0.947715 4.94772 0.5 5.5 0.5Z" stroke="${color}"/> `;
  let svgsolid = `<path d="M5.5 0C4.67157 0 4 0.671573 4 1.5V5.5C4 6.32843 4.67157 7 5.5 7H9.5C10.3284 7 11 6.32843 11 5.5V1.5C11 0.671573 10.3284 0 9.5 0H5.5Z" fill="${color}"/> <path d="M0 2H2V1H0V2Z" fill="${color}"/> <path d="M13 2H15V1H13V2Z" fill="${color}"/> <path d="M0 6H2V5H0V6Z" fill="${color}"/> <path d="M13 6H15V5H13V6Z" fill="${color}"/> <path d="M0 10H15V9H0V10Z" fill="${color}"/> <path d="M0 14H15V13H0V14Z" fill="${color}"/> `;
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
export let ariaLabel="float center" </script>

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
