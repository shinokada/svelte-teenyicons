<script lang="ts">
  export let size: string = "15";
  export let color: string = "black" 
  export let variation: "solid" | "outline" = "outline";
  let svgpath: string;
  let svgoutline = `<path d="M2 5.5H13M2 9.5H13M6.5 1.5L4.5 13.5M10.5 1.5L8.5 13.5" stroke="${color}"/> `;
  let svgsolid = `<path fill-rule="evenodd" clip-rule="evenodd" d="M5.40977 5L6.0068 1.4178L6.9932 1.5822L6.42356 5H9.40977L10.0068 1.4178L10.9932 1.5822L10.4236 5H13V6H10.2569L9.7569 9H13V10H9.59023L8.9932 13.5822L8.0068 13.4178L8.57644 10H5.59023L4.9932 13.5822L4.0068 13.4178L4.57644 10H2V9H4.7431L5.2431 6H2V5H5.40977ZM6.2569 6L5.7569 9H8.7431L9.2431 6H6.2569Z" fill="${color}"/> `;
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
export let ariaLabel="hashtag" </script>

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
