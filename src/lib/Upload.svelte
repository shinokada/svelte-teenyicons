<script lang="ts">
  export let size = "15";
  export let ariaLabel = "360";
  export let variation: "solid" | "outline" = "outline";
  let svgpath: string;
  let svgoutline = `<path d="M7.5 1.5L10.75 4.5M7.5 1.5L4.5 4.5M7.5 1.5V11M13.5 7V13.5H1.5V7" stroke="black"/> `;
  let svgsolid = `<path fill-rule="evenodd" clip-rule="evenodd" d="M7.48614 0.806747L11.0891 4.13259L10.4109 4.8674L8 2.64199V11H7V2.7071L4.85355 4.85355L4.14645 4.14644L7.48614 0.806747ZM2 13V6.99999H1V14H14V6.99999H13V13H2Z" fill="black"/> `;
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
