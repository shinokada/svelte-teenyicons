<script lang="ts">
  export let size = "15";
  export let ariaLabel = "360";
  export let variation: "solid" | "outline" = "outline";
  let svgpath: string;
  let svgoutline = `<path d="M15 14.5H0M15 0.5H0M13.5 9.5H1.5V5.5H13.5V9.5Z" stroke="black"/> `;
  let svgsolid = `<path d="M15 0H0V1H15V0Z" fill="black"/> <path d="M14 5H1V10H14V5Z" fill="black"/> <path d="M15 14H0V15H15V14Z" fill="black"/> `;
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
</script>

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
