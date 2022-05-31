<script lang="ts">
  export let size = "15";
  export let ariaLabel = "360";
  export let variation: "solid" | "outline" = "outline";
  let svgpath: string;
  let svgoutline = `<path d="M0.5 13.5C0.5 14.0523 0.947715 14.5 1.5 14.5C2.05228 14.5 2.5 14.0523 2.5 13.5C2.5 12.9477 2.05228 12.5 1.5 12.5C0.947715 12.5 0.5 12.9477 0.5 13.5Z" stroke="black"/> <path d="M14.5 15C14.5 6.99187 8.00813 0.5 0 0.5" stroke="black"/> <path d="M0 6.5C4.69442 6.5 8.5 10.3056 8.5 15" stroke="black"/> `;
  let svgsolid = `<path d="M14 15C14 7.26801 7.73199 1 0 1V0C8.28427 0 15 6.71573 15 15H14Z" fill="black"/> <path fill-rule="evenodd" clip-rule="evenodd" d="M0 13.5C0 12.6716 0.671573 12 1.5 12C2.32843 12 3 12.6716 3 13.5C3 14.3284 2.32843 15 1.5 15C0.671573 15 0 14.3284 0 13.5Z" fill="black"/> <path d="M9 15C9 10.0294 4.97056 6 0 6V7C4.41828 7 8 10.5817 8 15H9Z" fill="black"/> `;
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
