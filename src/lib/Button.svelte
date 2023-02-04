<script lang="ts">
  export let size: string = '15';
  export let color: string = 'black';
  export let variation: 'solid' | 'outline' = 'outline';
  let svgpath: string;
  let svgoutline = `<path d="M5.5 10V8.5M5.5 8.5V3.5C5.5 2.94772 5.94772 2.5 6.5 2.5C7.05228 2.5 7.5 2.94772 7.5 3.5V7.5H10.8529C11.7626 7.5 12.5 8.23741 12.5 9.14706V10C12.5 12.4853 10.4853 14.5 8 14.5H7.5C5.29086 14.5 3.5 12.7091 3.5 10.5C3.5 9.39543 4.39543 8.5 5.5 8.5ZM9 5.5H11C12.3807 5.5 13.5 4.38071 13.5 3C13.5 1.61929 12.3807 0.5 11 0.5H4C2.61929 0.5 1.5 1.61929 1.5 3C1.5 4.38071 2.61929 5.5 4 5.5" stroke="${color}"/> `;
  let svgsolid = `<path d="M4 6C2.34315 6 1 4.65685 1 3C1 1.34315 2.34315 0 4 0H11C12.6569 0 14 1.34315 14 3C14 4.65685 12.6569 6 11 6H9V3.5C9 2.11929 7.88071 1 6.5 1C5.11929 1 4 2.11929 4 3.5V6Z" fill="${color}"/> <path d="M6.5 2C5.67157 2 5 2.67157 5 3.5V8.05001C3.85888 8.28164 3 9.29052 3 10.5C3 12.9853 5.01472 15 7.5 15H8C10.7614 15 13 12.7614 13 10V9.14706C13 7.96127 12.0387 7 10.8529 7H8V3.5C8 2.67157 7.32843 2 6.5 2Z" fill="${color}"/> `;
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
  export let ariaLabel = 'button';
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
