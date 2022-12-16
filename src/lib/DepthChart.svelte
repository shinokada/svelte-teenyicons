<script lang="ts">
  export let size: string = '15';
  export let color: string = 'black';
  export let variation: 'solid' | 'outline' = 'outline';
  let svgpath: string;
  let svgoutline = `<path d="M0.5 0V14.5H14.5V0M0.5 4.5H2.5V5.5H4.5V8.5H6.5V11.5H7.5V14.5V12.5H9.5V10.5H11.5V7.5H12.5V5.5H14.5" stroke="${color}"/> `;
  let svgsolid = `<path d="M1 0H0V15H15V0H14V5H12V7H11V10H9V12H8V11H7V8H5V5H3V4H1V0Z" fill="${color}"/> `;
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
  export let ariaLabel = 'depth chart';
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
