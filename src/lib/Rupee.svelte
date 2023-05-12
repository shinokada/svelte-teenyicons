<script lang="ts">
  export let size: string = "15";
  export let color: string = "black" 
  export let variation: "solid" | "outline" = "outline";
  let svgpath: string;
  let svgoutline = `<path d="M2.5 8.5V8C2.29076 8 2.10365 8.13029 2.03106 8.32653C1.95846 8.52277 2.01574 8.74346 2.1746 8.87963L2.5 8.5ZM2 1H13V0H2V1ZM2.5 9H5.5V8H2.5V9ZM5.5 0H2.5V1H5.5V0ZM2.1746 8.87963L9.1746 14.8796L9.8254 14.1204L2.8254 8.12037L2.1746 8.87963ZM10 4.5C10 2.01472 7.98528 0 5.5 0V1C7.433 1 9 2.567 9 4.5H10ZM5.5 9C7.98528 9 10 6.98528 10 4.5H9C9 6.433 7.433 8 5.5 8V9ZM2 5H13V4H2V5Z" fill="${color}"/> `;
  let svgsolid = `<path fill-rule="evenodd" clip-rule="evenodd" d="M1.99999 1V0H13V1H8.32866C9.22627 1.72635 9.83888 2.791 9.97253 4H13V5H9.97253C9.72381 7.24998 7.81627 9 5.49999 9H3.85162L9.82539 14.1204L9.1746 14.8796L2.1746 8.87963C2.01573 8.74346 1.95846 8.52277 2.03105 8.32653C2.10365 8.13029 2.29076 8 2.49999 8H5.49999C7.26323 8 8.72193 6.69615 8.96455 5H1.99999V4H8.96455C8.72193 2.30385 7.26323 1 5.49999 1H1.99999Z" fill="${color}"/> `;
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
export let ariaLabel="rupee" </script>

<svg
  xmlns="http://www.w3.org/2000/svg"
  width={size}
  height={size}
  fill="none"
  class={$$props.class}
  {...$$restProps}
  aria-label={ariaLabel}
  viewBox="0 0 15 15"
  on:click 
  on:mouseenter 
  on:mouseleave 
  on:mouseover 
  on:mouseout 
  on:blur 
  on:focus 
>
  {@html svgpath}
</svg>
