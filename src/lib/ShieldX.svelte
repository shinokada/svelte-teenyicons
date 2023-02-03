<script lang="ts">
  export let size: string = "15";
  export let color: string = "black" 
  export let variation: "solid" | "outline" = "outline";
  let svgpath: string;
  let svgoutline = `<path d="M4.5 4.5L10.5 10.5M4.5 10.5L10.5 4.5M7.5 0.5L0.5 4.5V5.21989C0.5 9.52908 3.35661 13.3162 7.5 14.5C11.6434 13.3162 14.5 9.52908 14.5 5.21989V4.5L7.5 0.5Z" stroke="${color}" stroke-linejoin="round"/> `;
  let svgsolid = `<path fill-rule="evenodd" clip-rule="evenodd" d="M7.25193 0.0658784C7.40565 -0.0219595 7.59435 -0.0219595 7.74807 0.0658784L14.7481 4.06588C14.9039 4.1549 15 4.32057 15 4.5V5.21989C15 9.75232 11.9954 13.7356 7.63736 14.9808C7.54758 15.0064 7.45242 15.0064 7.36264 14.9808C3.0046 13.7356 0 9.75232 0 5.21989V4.5C0 4.32057 0.096143 4.1549 0.251931 4.06588L7.25193 0.0658784ZM10.1465 10.8536L7.50004 8.20711L4.85359 10.8536L4.14648 10.1465L6.79293 7.50001L4.14648 4.85356L4.85359 4.14645L7.50004 6.7929L10.1465 4.14645L10.8536 4.85356L8.20714 7.50001L10.8536 10.1465L10.1465 10.8536Z" fill="${color}"/> `;
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
export let ariaLabel="shield x" </script>

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
