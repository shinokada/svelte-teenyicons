<script lang="ts">
  export let size = "15";
  export let ariaLabel = "360";
  export let variation: "solid" | "outline" = "outline";
  let svgpath: string;
  let svgoutline = `<path d="M4 14.5H11M7.5 14.5V9.5M7.5 9.5C9.70914 9.5 11.5 7.70914 11.5 5.5V1.5C11.5 0.947715 11.0523 0.5 10.5 0.5H4.5C3.94772 0.5 3.5 0.947715 3.5 1.5V5.5C3.5 7.70914 5.29086 9.5 7.5 9.5ZM3.5 2.5H2.5C1.39543 2.5 0.5 3.39543 0.5 4.5C0.5 5.60457 1.39543 6.5 2.5 6.5H3.5M11.5 2.5H12.5C13.6046 2.5 14.5 3.39543 14.5 4.5C14.5 5.60457 13.6046 6.5 12.5 6.5H11.5" stroke="black"/> `;
  let svgsolid = `<path fill-rule="evenodd" clip-rule="evenodd" d="M4.5 0C3.67157 0 3 0.671573 3 1.5V2H2.5C1.11929 2 0 3.11929 0 4.5C0 5.88071 1.11929 7 2.5 7H3.25606C3.82053 8.59703 5.26092 9.78029 7 9.97254V14H4V15H11V14H8V9.97254C9.73908 9.78029 11.1795 8.59703 11.7439 7H12.5C13.8807 7 15 5.88071 15 4.5C15 3.11929 13.8807 2 12.5 2H12V1.5C12 0.671573 11.3284 0 10.5 0H4.5ZM12 3V5.5C12 5.669 11.9907 5.83583 11.9725 6H12.5C13.3284 6 14 5.32843 14 4.5C14 3.67157 13.3284 3 12.5 3H12ZM2.5 3H3V5.5C3 5.669 3.00932 5.83583 3.02746 6H2.5C1.67157 6 1 5.32843 1 4.5C1 3.67157 1.67157 3 2.5 3Z" fill="black"/> `;
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
