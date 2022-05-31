<script lang="ts">
  export let size = "15";
  export let ariaLabel = "360";
  export let variation: "solid" | "outline" = "outline";
  let svgpath: string;
  let svgoutline = `<path d="M2.5 4.5C1.39543 4.5 0.5 3.60457 0.5 2.5C0.5 1.39543 1.39543 0.5 2.5 0.5C3.60457 0.5 4.5 1.39543 4.5 2.5C4.5 3.60457 3.60457 4.5 2.5 4.5ZM2.5 4.5V10.5M2.5 10.5C3.60457 10.5 4.5 11.3954 4.5 12.5C4.5 13.6046 3.60457 14.5 2.5 14.5C1.39543 14.5 0.5 13.6046 0.5 12.5C0.5 11.3954 1.39543 10.5 2.5 10.5ZM12.5 4.5C11.3954 4.5 10.5 3.60457 10.5 2.5C10.5 1.39543 11.3954 0.5 12.5 0.5C13.6046 0.5 14.5 1.39543 14.5 2.5C14.5 3.60457 13.6046 4.5 12.5 4.5ZM12.5 4.5V5.5C12.5 7.15685 11.1569 8.5 9.5 8.5H2.5" stroke="black"/> `;
  let svgsolid = `<path d="M2.5 0C1.11929 0 0 1.11929 0 2.5C0 3.70948 0.85888 4.71836 2 4.94999V10.05C0.85888 10.2816 0 11.2905 0 12.5C0 13.8807 1.11929 15 2.5 15C3.88071 15 5 13.8807 5 12.5C5 11.2905 4.14112 10.2816 3 10.05V9H9.5C11.433 9 13 7.433 13 5.5V4.94999C14.1411 4.71836 15 3.70948 15 2.5C15 1.11929 13.8807 0 12.5 0C11.1193 0 10 1.11929 10 2.5C10 3.70948 10.8589 4.71836 12 4.94999V5.5C12 6.88071 10.8807 8 9.5 8H3V4.94999C4.14112 4.71836 5 3.70948 5 2.5C5 1.11929 3.88071 0 2.5 0Z" fill="black"/> `;
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
