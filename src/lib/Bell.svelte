<script lang="ts">
  export let size: string = '15';
  export let color: string = 'black';
  export let variation: 'solid' | 'outline' = 'outline';
  let svgpath: string;
  let svgoutline = `<path d="M1 10.5H14M2.5 10.5V5.5C2.5 2.73858 4.73858 0.5 7.5 0.5C10.2614 0.5 12.5 2.73858 12.5 5.5V10.5M5.5 12V12.5C5.5 13.6046 6.39543 14.5 7.5 14.5C8.60457 14.5 9.5 13.6046 9.5 12.5V12" stroke="${color}"/> `;
  let svgsolid = `<path d="M7.5 0C4.46243 0 2 2.46243 2 5.5V10H1V11H14V10H13V5.5C13 2.46243 10.5376 0 7.5 0Z" fill="${color}"/> <path d="M5 12.5V12H10V12.5C10 13.8807 8.88071 15 7.5 15C6.11929 15 5 13.8807 5 12.5Z" fill="${color}"/> `;
  switch (variation) {
    case 'outline':
      svgpath = svgoutline;
      break;
    case 'solid':
      svgpath = svgsolid;
      break;
    default:
      svgpath = svgoutline;
  }
  export let ariaLabel = 'bell';
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
