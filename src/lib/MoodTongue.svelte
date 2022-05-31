<script lang="ts">
  export let size = "15";
  export let ariaLabel = "360";
  export let variation: "solid" | "outline" = "outline";
  let svgpath: string;
  let svgoutline = `<path d="M4 5.5H5M10 5.5H11M4 8.5H11M5.5 8.5V10.5C5.5 11.6046 6.39543 12.5 7.5 12.5C8.60457 12.5 9.5 11.6046 9.5 10.5V8.5M7.5 14.5C3.63401 14.5 0.5 11.366 0.5 7.5C0.5 3.63401 3.63401 0.5 7.5 0.5C11.366 0.5 14.5 3.63401 14.5 7.5C14.5 11.366 11.366 14.5 7.5 14.5Z" stroke="black"/> `;
  let svgsolid = `<path d="M6 10.5V9H9V10.5C9 11.3284 8.32843 12 7.5 12C6.67157 12 6 11.3284 6 10.5Z" fill="black"/> <path fill-rule="evenodd" clip-rule="evenodd" d="M0 7.5C0 3.35786 3.35786 0 7.5 0C11.6421 0 15 3.35786 15 7.5C15 11.6421 11.6421 15 7.5 15C3.35786 15 0 11.6421 0 7.5ZM5 6H4V5H5V6ZM11 6H10V5H11V6ZM4 9H5V10.5C5 11.8807 6.11929 13 7.5 13C8.88071 13 10 11.8807 10 10.5V9H11V8H4V9Z" fill="black"/> `;
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
