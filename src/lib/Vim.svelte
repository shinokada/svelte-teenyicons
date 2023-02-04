<script lang="ts">
  export let size: string = '15';
  export let color: string = 'black';
  export let variation: 'solid' | 'outline' = 'outline';
  let svgpath: string;
  let svgoutline = `<path d="M1.5 3.5H2.5V13.5H5.5L13.5 3.5V1.5H8.5V3.5H10.5L5.5 9.5V3.5H6.5V1.5H1.5V3.5Z" stroke="${color}"/> `;
  let svgsolid = `<path d="M7 1H1V4H2V14H5.74031L14 3.67539V1H8V4H9.43248L6 8.11898V4H7V1Z" fill="${color}"/> `;
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
  export let ariaLabel = 'vim';
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
