<script lang="ts">
  export let size: string = "15";
  export let color: string = "black" 
  export let variation: "solid" | "outline" = "outline";
  let svgpath: string;
  let svgoutline = `<path d="M0.5 12.5V2.5L7.5 7.5L0.5 12.5Z" stroke="${color}" stroke-linejoin="round"/> <path d="M7.5 12.5V2.5L14.5 7.5L7.5 12.5Z" stroke="${color}" stroke-linejoin="round"/> `;
  let svgsolid = `<path d="M0.790619 2.09314C0.638212 1.98427 0.437745 1.96972 0.271209 2.05542C0.104674 2.14112 0 2.31271 0 2.5V12.5C0 12.6873 0.104674 12.8589 0.271209 12.9446C0.437745 13.0303 0.638212 13.0157 0.790619 12.9069L7 8.4716V12.5C7 12.6873 7.10467 12.8589 7.27121 12.9446C7.43774 13.0303 7.63821 13.0157 7.79062 12.9069L14.7906 7.90687C14.922 7.81301 15 7.66148 15 7.5C15 7.33853 14.922 7.18699 14.7906 7.09314L7.79062 2.09314C7.63821 1.98427 7.43774 1.96972 7.27121 2.05542C7.10467 2.14112 7 2.31271 7 2.5V6.52841L0.790619 2.09314Z" fill="${color}"/> `;
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
export let ariaLabel="forward" </script>

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
