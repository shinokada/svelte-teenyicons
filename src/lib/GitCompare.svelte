<script lang="ts">
  export let size: string = "15";
  export let color: string = "black" 
  export let variation: "solid" | "outline" = "outline";
  let svgpath: string;
  let svgoutline = `<path d="M8.5 0.5L6.5 2.5M6.5 2.5L8.5 4.5M6.5 2.5H9.5C11.1569 2.5 12.5 3.84315 12.5 5.5V10.5M2.5 4.5C3.60457 4.5 4.5 3.60457 4.5 2.5C4.5 1.39543 3.60457 0.5 2.5 0.5C1.39543 0.5 0.5 1.39543 0.5 2.5C0.5 3.60457 1.39543 4.5 2.5 4.5ZM2.5 4.5V9.5C2.5 11.1569 3.84315 12.5 5.5 12.5H8M6.5 14.5L8.5 12.5L6.5 10.5M12.5 10.5C11.3954 10.5 10.5 11.3954 10.5 12.5C10.5 13.6046 11.3954 14.5 12.5 14.5C13.6046 14.5 14.5 13.6046 14.5 12.5C14.5 11.3954 13.6046 10.5 12.5 10.5Z" stroke="${color}"/> `;
  let svgsolid = `<path d="M2.5 0C1.11929 0 0 1.11929 0 2.5C0 3.70948 0.85888 4.71836 2 4.94999V9.5C2 11.433 3.567 13 5.5 13H7.29289L6.14645 14.1464L6.85355 14.8536L9.20711 12.5L6.85355 10.1464L6.14645 10.8536L7.29289 12H5.5C4.11929 12 3 10.8807 3 9.5V4.94999C4.14112 4.71836 5 3.70948 5 2.5C5 1.11929 3.88071 0 2.5 0Z" fill="${color}"/> <path d="M8.85355 0.853554L8.14645 0.146446L5.79289 2.5L8.14645 4.85355L8.85355 4.14645L7.70711 3H9.5C10.8807 3 12 4.11929 12 5.5V10.05C10.8589 10.2816 10 11.2905 10 12.5C10 13.8807 11.1193 15 12.5 15C13.8807 15 15 13.8807 15 12.5C15 11.2905 14.1411 10.2816 13 10.05V5.5C13 3.567 11.433 2 9.5 2H7.70711L8.85355 0.853554Z" fill="${color}"/> `;
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
export let ariaLabel="git compare" </script>

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
