<script lang="ts">
  export let size: string = "15";
  export let color: string = "black" 
  export let variation: "solid" | "outline" = "outline";
  let svgpath: string;
  let svgoutline = `<path d="M9 5.5H15M9 1.5H15M0 9.5H15M0 13.5H15M1.5 0.5H5.5C6.05228 0.5 6.5 0.947715 6.5 1.5V5.5C6.5 6.05228 6.05228 6.5 5.5 6.5H1.5C0.947715 6.5 0.5 6.05228 0.5 5.5V1.5C0.5 0.947715 0.947715 0.5 1.5 0.5Z" stroke="${color}"/> `;
  let svgsolid = `<path d="M1.5 0C0.671573 0 0 0.671573 0 1.5V5.5C0 6.32843 0.671573 7 1.5 7H5.5C6.32843 7 7 6.32843 7 5.5V1.5C7 0.671573 6.32843 0 5.5 0H1.5Z" fill="${color}"/> <path d="M9 2H15V1H9V2Z" fill="${color}"/> <path d="M9 6H15V5H9V6Z" fill="${color}"/> <path d="M0 10H15V9H0V10Z" fill="${color}"/> <path d="M0 14H15V13H0V14Z" fill="${color}"/> `;
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
export let ariaLabel="float left" </script>

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
