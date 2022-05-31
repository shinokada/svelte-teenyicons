<script lang="ts">
  export let size = "15";
  export let ariaLabel = "360";
  export let variation: "solid" | "outline" = "outline";
  let svgpath: string;
  let svgoutline = `<path d="M2 13.5H13M7.5 10.5V14M14.1896 11.4113C9.81735 10.1621 5.18265 10.1621 0.810401 11.4113C0.654846 11.4558 0.5 11.339 0.5 11.1772L0.5 1.82282C0.5 1.66104 0.654846 1.54424 0.810401 1.58868C5.18265 2.8379 9.81735 2.8379 14.1896 1.58868C14.3452 1.54424 14.5 1.66104 14.5 1.82282V11.1772C14.5 11.339 14.3452 11.4558 14.1896 11.4113Z" stroke="black"/> `;
  let svgsolid = `<path d="M0.947762 1.10792C0.472799 0.972213 0 1.32885 0 1.82281V11.1772C0 11.6711 0.472801 12.0278 0.947762 11.8921C2.92718 11.3265 4.96152 11.0224 7 10.9796V13H2V14H13V13H8V10.9796C10.0385 11.0224 12.0728 11.3265 14.0522 11.8921C14.5272 12.0278 15 11.6711 15 11.1772V1.82282C15 1.32885 14.5272 0.972214 14.0522 1.10792C9.76976 2.33148 5.23024 2.33148 0.947762 1.10792Z" fill="black"/> `;
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
