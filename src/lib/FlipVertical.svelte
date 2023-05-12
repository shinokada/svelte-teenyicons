<script lang="ts">
  export let size: string = "15";
  export let color: string = "black" 
  export let variation: "solid" | "outline" = "outline";
  let svgpath: string;
  let svgoutline = `<path d="M4.5 3.5H5C5 3.26811 4.84056 3.06665 4.61488 3.01338C4.38919 2.9601 4.15649 3.06899 4.05279 3.27639L4.5 3.5ZM4.5 11.5V12C4.77614 12 5 11.7761 5 11.5H4.5ZM0.5 11.5L0.0527864 11.2764C-0.0247107 11.4314 -0.0164287 11.6155 0.0746746 11.7629C0.165778 11.9103 0.326711 12 0.5 12L0.5 11.5ZM10.5 3.5L10.9472 3.27639C10.8435 3.06899 10.6108 2.9601 10.3851 3.01338C10.1594 3.06665 10 3.26811 10 3.5H10.5ZM10.5 11.5H10C10 11.7761 10.2239 12 10.5 12V11.5ZM14.5 11.5V12C14.6733 12 14.8342 11.9103 14.9253 11.7629C15.0164 11.6155 15.0247 11.4314 14.9472 11.2764L14.5 11.5ZM4 3.5V11.5H5V3.5H4ZM4.5 11H0.5V12H4.5V11ZM0.947214 11.7236L4.94721 3.72361L4.05279 3.27639L0.0527864 11.2764L0.947214 11.7236ZM10 3.5V11.5H11V3.5H10ZM10.5 12H14.5V11H10.5V12ZM14.9472 11.2764L10.9472 3.27639L10.0528 3.72361L14.0528 11.7236L14.9472 11.2764ZM7 0V15H8V0H7Z" fill="${color}"/> `;
  let svgsolid = `<path d="M7 0V15H8V0H7Z" fill="${color}"/> <path d="M4.61488 3.01342C4.84056 3.0667 5 3.26816 5 3.50005V11.5C5 11.7762 4.77614 12 4.5 12H0.500001C0.326712 12 0.165778 11.9103 0.0746751 11.7629C-0.0164282 11.6155 -0.0247102 11.4314 0.0527869 11.2764L4.05279 3.27644C4.15649 3.06903 4.38919 2.96015 4.61488 3.01342Z" fill="${color}"/> <path d="M10.3851 3.01342C10.6108 2.96015 10.8435 3.06903 10.9472 3.27644L14.9472 11.2764C15.0247 11.4314 15.0164 11.6155 14.9253 11.7629C14.8342 11.9103 14.6733 12 14.5 12H10.5C10.2239 12 10 11.7762 10 11.5V3.50005C10 3.26816 10.1594 3.0667 10.3851 3.01342Z" fill="${color}"/> `;
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
export let ariaLabel="flip vertical" </script>

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
