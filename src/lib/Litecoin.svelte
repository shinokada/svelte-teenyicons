<script lang="ts">
  export let size: string = "15";
  export let color: string = "black" 
  export let variation: "solid" | "outline" = "outline";
  let svgpath: string;
  let svgoutline = `<path d="M5.5 1.5L2.5 13.5H13M1 8.5L7 5.5" stroke="${color}"/> `;
  let svgsolid = `<path fill-rule="evenodd" clip-rule="evenodd" d="M3.71354 6.58419L5.0149 1.37872L5.98504 1.62126L4.89157 5.99518L6.77637 5.05278L7.22358 5.9472L4.57213 7.27293L3.14036 13H13V14H1.85959L3.3941 7.86195L1.22358 8.9472L0.776367 8.05278L3.71354 6.58419Z" fill="${color}"/> `;
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
export let ariaLabel="litecoin" </script>

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
