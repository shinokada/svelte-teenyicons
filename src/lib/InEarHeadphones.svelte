<script lang="ts">
  export let size: string = "15";
  export let color: string = "black" 
  export let variation: "solid" | "outline" = "outline";
  let svgpath: string;
  let svgoutline = `<path d="M14.5 12.5V13H15V12.5H14.5ZM12.5 12.5H12V13H12.5V12.5ZM0.5 12.5H0V13H0.5V12.5ZM2.5 12.5V13H3V12.5H2.5ZM10 5V1.65385H9V5H10ZM14 3.5V12.5H15V3.5H14ZM14.5 12H12.5V13H14.5V12ZM12.5 6H11V7H12.5V6ZM10.6538 1H11.5V0H10.6538V1ZM11 6C10.4477 6 10 5.55228 10 5H9C9 6.10457 9.89543 7 11 7V6ZM15 3.5C15 1.567 13.433 0 11.5 0V1C12.8807 1 14 2.11929 14 3.5H15ZM10 1.65385C10 1.29274 10.2927 1 10.6538 1V0C9.74045 0 9 0.740453 9 1.65385H10ZM13 12.5V15H14V12.5H13ZM6 5V1.65385H5V5H6ZM0 3.5V12.5H1V3.5H0ZM0.5 13H2.5V12H0.5V13ZM2.5 7H4V6H2.5V7ZM4.34615 0H3.5V1H4.34615V0ZM4 7C5.10457 7 6 6.10457 6 5H5C5 5.55228 4.55228 6 4 6V7ZM1 3.5C1 2.11929 2.11929 1 3.5 1V0C1.567 0 0 1.567 0 3.5H1ZM6 1.65385C6 0.740452 5.25955 0 4.34615 0V1C4.70726 1 5 1.29274 5 1.65385H6ZM1 12.5V15H2V12.5H1ZM12 4V6.5H13V4H12ZM2 4V6.5H3V4H2ZM13 12.5V6.5H12V12.5H13ZM3 12.5V6.5H2V12.5H3Z" fill="${color}"/> `;
  let svgsolid = `<path d="M6 1.65385C6 0.740453 5.25955 0 4.34615 0H3.5C1.567 0 0 1.567 0 3.5V13H1V15H2V13H3V7H4C5.10457 7 6 6.10457 6 5V1.65385Z" fill="${color}"/> <path d="M10.6538 0C9.74045 0 9 0.740453 9 1.65385V5C9 6.10457 9.89543 7 11 7H12V13H13V15H14V13H15V3.5C15 1.567 13.433 0 11.5 0H10.6538Z" fill="${color}"/> `;
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
export let ariaLabel="in ear headphones" </script>

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
