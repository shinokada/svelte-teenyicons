<script lang="ts">
  export let size: string = "15";
  export let color: string = "black" 
  export let variation: "solid" | "outline" = "outline";
  let svgpath: string;
  let svgoutline = `<path d="M8 1L1 7.5L8 14M13.5 1L6.5 7.5L13.5 14" stroke="${color}" stroke-linecap="square"/> `;
  let svgsolid = `<path fill-rule="evenodd" clip-rule="evenodd" d="M8.70665 1.02619L1.73483 7.50002L8.70665 13.9738L8.02619 14.7066L0.265217 7.50002L8.0262 0.293396L8.70665 1.02619ZM14.2066 1.02619L7.23483 7.50002L14.2066 13.9738L13.5262 14.7066L5.76522 7.50002L13.5262 0.293396L14.2066 1.02619Z" fill="${color}"/> `;
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
export let ariaLabel="double caret left" </script>

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
