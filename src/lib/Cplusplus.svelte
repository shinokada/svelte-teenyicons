<script lang="ts">
  export let size: string = "15";
  export let color: string = "black" 
  export let variation: "solid" | "outline" = "outline";
  let svgpath: string;
  let svgoutline = `<path d="M9.5 9.5C8.85971 10.1403 7.99129 10.5 7.08579 10.5H6.5C4.84315 10.5 3.5 9.15685 3.5 7.5C3.5 5.84315 4.84315 4.5 6.5 4.5H7.08579C7.99129 4.5 8.85971 4.85971 9.5 5.5M7.5 6V9M6 7.5H12M10.5 6V9M1.5 10.5V4.5L7.5 1L13.5 4.5V10.5L7.5 14L1.5 10.5Z" stroke="${color}"/> `;
  let svgsolid = `<path fill-rule="evenodd" clip-rule="evenodd" d="M7.5 0.421143L14 4.21281V10.7872L7.5 14.5788L1 10.7872V4.21281L7.5 0.421143ZM6.5 4C4.567 4 3 5.567 3 7.5C3 9.433 4.567 11 6.5 11H7.08579C8.1239 11 9.1195 10.5876 9.85355 9.85355L9.14645 9.14645C8.59993 9.69297 7.85868 10 7.08579 10H6.5C5.11929 10 4 8.88071 4 7.5C4 6.11929 5.11929 5 6.5 5H7.08579C7.85868 5 8.59993 5.30703 9.14645 5.85355L9.85355 5.14645C9.1195 4.41239 8.1239 4 7.08579 4H6.5ZM7 7V6H8V7H10V6H11V7H12V8H11V9H10V8H8V9H7V8H6V7H7Z" fill="${color}"/> `;
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
export let ariaLabel="cplusplus" </script>

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
