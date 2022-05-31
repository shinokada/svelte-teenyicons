<script lang="ts">
  export let size = "15";
  export let ariaLabel = "360";
  export let variation: "solid" | "outline" = "outline";
  let svgpath: string;
  let svgoutline = `<path d="M0.5 14.5L5 10M0.5 5.5L9.5 14.5M8.5 0.5L14.5 6.5M1.5 6.5L9.5 1.5M8.5 13.5L13.5 5.5" stroke="black"/> `;
  let svgsolid = `<path d="M8.70206 1.40917L8.14648 0.853591L8.85359 0.146484L14.8536 6.14648L14.1465 6.85359L13.5908 6.29795L9.13477 13.4277L9.85359 14.1465L9.14648 14.8536L5.00004 10.7071L0.853591 14.8536L0.146484 14.1465L4.29293 10L0.146484 5.85359L0.853591 5.14648L1.57235 5.86524L8.70206 1.40917Z" fill="black"/> `;
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
