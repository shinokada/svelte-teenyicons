<script lang="ts">
  export let size: string = "15";
  export let color: string = "black" 
  export let variation: "solid" | "outline" = "outline";
  let svgpath: string;
  let svgoutline = `<path d="M11.5 6V5.83333C11.5 5.09695 10.903 4.5 10.1667 4.5H9C8.17157 4.5 7.5 5.17157 7.5 6C7.5 6.82843 8.17157 7.5 9 7.5H10C10.8284 7.5 11.5 8.17157 11.5 9C11.5 9.82843 10.8284 10.5 10 10.5H9C8.17157 10.5 7.5 9.82843 7.5 9M5.5 4V9.26393C5.5 10.0215 5.072 10.714 4.39443 11.0528L3.5 11.5M1.5 10.5V4.5L7.5 1L13.5 4.5V10.5L7.5 14L1.5 10.5Z" stroke="${color}"/> `;
  let svgsolid = `<path fill-rule="evenodd" clip-rule="evenodd" d="M14 4.21281L7.5 0.421143L1 4.21281V10.7872L2.00634 11.3742L4.06264 10.5422C4.62921 10.313 5.00004 9.7629 5.00004 9.15171V4H6.00004V9.15171C6.00004 10.1704 5.382 11.0871 4.43772 11.4692L3.09826 12.0112L7.5 14.5788L14 10.7872V4.21281ZM7 6C7 4.89543 7.89543 4 9 4H10.1667C11.1792 4 12 4.82081 12 5.83333V6H11V5.83333C11 5.3731 10.6269 5 10.1667 5H9C8.44772 5 8 5.44772 8 6C8 6.55228 8.44772 7 9 7H10C11.1046 7 12 7.89543 12 9C12 10.1046 11.1046 11 10 11H9C7.89543 11 7 10.1046 7 9H8C8 9.55228 8.44772 10 9 10H10C10.5523 10 11 9.55228 11 9C11 8.44772 10.5523 8 10 8H9C7.89543 8 7 7.10457 7 6Z" fill="${color}"/> `;
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
export let ariaLabel="nodejs" </script>

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
