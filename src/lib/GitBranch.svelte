<script lang="ts">
  export let size: string = "15";
  export let color: string = "black" 
  export let variation: "solid" | "outline" = "outline";
  let svgpath: string;
  let svgoutline = `<path d="M2.5 4.5C1.39543 4.5 0.5 3.60457 0.5 2.5C0.5 1.39543 1.39543 0.5 2.5 0.5C3.60457 0.5 4.5 1.39543 4.5 2.5C4.5 3.60457 3.60457 4.5 2.5 4.5ZM2.5 4.5V10.5M4.5 12.5C4.5 13.6046 3.60457 14.5 2.5 14.5C1.39543 14.5 0.5 13.6046 0.5 12.5C0.5 11.3954 1.39543 10.5 2.5 10.5M4.5 12.5C4.5 11.3954 3.60457 10.5 2.5 10.5M4.5 12.5H9.5C11.1569 12.5 12.5 11.1569 12.5 9.5V7.5M12.5 7.5C11.3954 7.5 10.5 6.60457 10.5 5.5C10.5 4.39543 11.3954 3.5 12.5 3.5C13.6046 3.5 14.5 4.39543 14.5 5.5C14.5 6.60457 13.6046 7.5 12.5 7.5Z" stroke="${color}"/> `;
  let svgsolid = `<path d="M2.5 0C1.11929 0 0 1.11929 0 2.5C0 3.70948 0.85888 4.71836 2 4.94999V10.05C0.85888 10.2816 0 11.2905 0 12.5C0 13.8807 1.11929 15 2.5 15C3.70948 15 4.71836 14.1411 4.94999 13H9.5C11.433 13 13 11.433 13 9.5V7.94999C14.1411 7.71836 15 6.70948 15 5.5C15 4.11929 13.8807 3 12.5 3C11.1193 3 10 4.11929 10 5.5C10 6.70948 10.8589 7.71836 12 7.94999V9.5C12 10.8807 10.8807 12 9.5 12H4.94999C4.75115 11.0204 3.97957 10.2488 3 10.05V4.94999C4.14112 4.71836 5 3.70948 5 2.5C5 1.11929 3.88071 0 2.5 0Z" fill="${color}"/> `;
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
export let ariaLabel="git branch" </script>

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
