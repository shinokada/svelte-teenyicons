<script lang="ts">
  export let size = "15";
  export let ariaLabel = "360";
  export let variation: "solid" | "outline" = "outline";
  let svgpath: string;
  let svgoutline = `<path d="M14.5 7V15M0.5 7V15M0 10.5H15M0 7.5H15M2 5.5H6M9 5.5H13M0.5 6V0.5H14.5V6" stroke="black"/> `;
  let svgsolid = `<path d="M0 0H15V6H14V1H1V6H0V0Z" fill="black"/> <path d="M6 6H2V5H6V6Z" fill="black"/> <path d="M0 15H1V11H14V15H15V7H0V15Z" fill="black"/> <path d="M9 6H13V5H9V6Z" fill="black"/> `;
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
