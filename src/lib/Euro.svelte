<script lang="ts">
  export let size: string = "15";
  export let color: string = "black" 
  export let variation: "solid" | "outline" = "outline";
  let svgpath: string;
  let svgoutline = `<path d="M13.374 3C12.2848 1.48593 10.5075 0.5 8.5 0.5C5.18629 0.5 2.5 3.18629 2.5 6.5V8.5C2.5 11.8137 5.18629 14.5 8.5 14.5C10.5075 14.5 12.2848 13.5141 13.374 12M0 5.5H7M0 9.5H7" stroke="${color}"/> `;
  let svgsolid = `<path fill-rule="evenodd" clip-rule="evenodd" d="M2.17393 5C2.8511 2.1333 5.42642 0 8.5 0C10.6752 0 12.6008 1.06896 13.7798 2.70802L12.9681 3.29198C11.9688 1.9029 10.3398 1 8.5 1C5.98245 1 3.85996 2.6915 3.20703 5H7V6H3.02242C3.00758 6.16468 3 6.33145 3 6.5V8.5C3 8.66854 3.00758 8.83532 3.02242 9H7V10H3.20703C3.85996 12.3085 5.98245 14 8.5 14C10.3398 14 11.9688 13.0971 12.9681 11.708L13.7798 12.292C12.6008 13.931 10.6752 15 8.5 15C5.42642 15 2.8511 12.8667 2.17393 10H0V9H2.01894C2.00639 8.83498 2 8.66824 2 8.5V6.5C2 6.33176 2.00639 6.16502 2.01894 6H0V5H2.17393Z" fill="${color}"/> `;
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
export let ariaLabel="euro" </script>

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
