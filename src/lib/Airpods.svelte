<script lang="ts">
  export let size: string = "15";
  export let color: string = "black" 
  export let variation: "solid" | "outline" = "outline";
  let svgpath: string;
  let svgoutline = `<path d="M6.5 3.49999C6.5 5.09297 5.10384 6.32547 3.52317 6.12789L3.20273 6.08783C2.74222 6.03027 2.30471 5.85353 1.93344 5.57508L0.5 4.49999V2.49999L1.93344 1.42491C2.30471 1.14646 2.74222 0.969716 3.20273 0.912153L3.52317 0.872098C5.10384 0.674514 6.5 1.90702 6.5 3.49999ZM6.5 3.49999V14.5H4.5V5.99999M8.5 3.49999C8.5 5.09297 9.89616 6.32547 11.4768 6.12789L11.7973 6.08783C12.2578 6.03027 12.6953 5.85353 13.0666 5.57508L14.5 4.49999V2.49999L13.0666 1.42491C12.6953 1.14646 12.2578 0.969716 11.7973 0.912153L11.4768 0.872098C9.89616 0.674514 8.5 1.90702 8.5 3.49999ZM8.5 3.49999V14.5H10.5V5.99999M2 3.49999H4M11 3.49999H13" stroke="${color}"/> `;
  let svgsolid = `<path fill-rule="evenodd" clip-rule="evenodd" d="M7 3.50001C7 1.60628 5.34025 0.141084 3.46115 0.375972L3.14071 0.416027C2.59386 0.484383 2.07432 0.694263 1.63344 1.02492L0 2.25001V4.75001L1.63344 5.97509C2.07432 6.30575 2.59386 6.51563 3.14071 6.58399L3.46115 6.62404C3.64326 6.64681 3.82332 6.6536 4 6.64559V15H7V3.50001ZM4 4H2V3H4V4Z" fill="${color}"/> <path fill-rule="evenodd" clip-rule="evenodd" d="M8 3.50001C8 1.60628 9.65975 0.141084 11.5389 0.375972L11.8593 0.416027C12.4061 0.484383 12.9257 0.694263 13.3666 1.02492L15 2.25001V4.75001L13.3666 5.97509C12.9257 6.30575 12.4061 6.51563 11.8593 6.58399L11.5389 6.62404C11.3567 6.64681 11.1767 6.6536 11 6.64559V15H8V3.50001ZM11 4H13V3H11V4Z" fill="${color}"/> `;
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
export let ariaLabel="airpods" </script>

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
