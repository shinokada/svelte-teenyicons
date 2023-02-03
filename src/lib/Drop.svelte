<script lang="ts">
  export let size: string = "15";
  export let color: string = "black" 
  export let variation: "solid" | "outline" = "outline";
  let svgpath: string;
  let svgoutline = `<path d="M7.5 0.5L11.7857 4.64226C12.6126 5.45792 13.1719 6.49138 13.3935 7.61304C13.6151 8.73469 13.4892 9.89463 13.0315 10.9474C12.5738 12.0001 11.8047 12.8989 10.8207 13.5309C9.83665 14.1629 8.68147 14.5 7.5 14.5C6.31853 14.5 5.16335 14.1629 4.17932 13.5309C3.19529 12.8989 2.42621 12.0001 1.96851 10.9474C1.51082 9.89463 1.38489 8.73469 1.6065 7.61304C1.82812 6.49138 2.38743 5.45792 3.21429 4.64226L7.5 0.5Z" stroke="${color}" stroke-linecap="round" stroke-linejoin="round"/> `;
  let svgsolid = `<path d="M7.84749 0.140481C7.65369 -0.046827 7.34631 -0.046827 7.15252 0.140481L2.86679 4.28272L2.86315 4.28631C1.96612 5.1712 1.35737 6.29444 1.11599 7.51612C0.874584 8.73792 1.01193 10.0012 1.50997 11.1467C2.00793 12.2921 2.84344 13.2671 3.90912 13.9516C4.97463 14.6359 6.22377 15 7.5 15C8.77624 15 10.0254 14.6359 11.0909 13.9516C12.1566 13.2671 12.9921 12.2921 13.49 11.1467C13.9881 10.0012 14.1254 8.73792 13.884 7.51612C13.6426 6.29444 13.0339 5.17118 12.1369 4.28629L7.84749 0.140481Z" fill="${color}"/> `;
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
export let ariaLabel="drop" </script>

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
