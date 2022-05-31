<script lang="ts">
  export let size = "15";
  export let ariaLabel = "360";
  export let variation: "solid" | "outline" = "outline";
  let svgpath: string;
  let svgoutline = `<path d="M0.5 7.5C0.5 3.63401 3.63401 0.5 7.5 0.5C11.366 0.5 14.5 3.63401 14.5 7.5C14.5 11.366 11.366 14.5 7.5 14.5C3.63401 14.5 0.5 11.366 0.5 7.5Z" stroke="black"/> <path d="M9.5 5.5H5.5V9.5H9.5V5.5Z" stroke="black"/> `;
  let svgsolid = `<path fill-rule="evenodd" clip-rule="evenodd" d="M0 7.5C0 3.35786 3.35786 0 7.5 0C11.6421 0 15 3.35786 15 7.5C15 11.6421 11.6421 15 7.5 15C3.35786 15 0 11.6421 0 7.5ZM5 5H10V10H5V5Z" fill="black"/> `;
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
