<script lang="ts">
  export let size = "15";
  export let ariaLabel = "360";
  export let variation: "solid" | "outline" = "outline";
  let svgpath: string;
  let svgoutline = `<path d="M15 14.5H0M11.5 11.5H8.5V4.5H11.5V11.5ZM6.5 11.5H3.5V0.5H6.5V11.5Z" stroke="black"/> `;
  let svgsolid = `<path d="M7 0H3V12H7V0Z" fill="black"/> <path d="M12 4H8V12H12V4Z" fill="black"/> <path d="M15 14H0V15H15V14Z" fill="black"/> `;
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
