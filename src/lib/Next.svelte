<script lang="ts">
  export let size: string = '15';
  export let color: string = 'black';
  export let variation: 'solid' | 'outline' = 'outline';
  let svgpath: string;
  let svgoutline = `<path d="M1.5 2.5L1.79062 2.09313C1.63821 1.98427 1.43774 1.96971 1.27121 2.05542C1.10467 2.14112 1 2.31271 1 2.5H1.5ZM1.5 12.5H1C1 12.6873 1.10467 12.8589 1.27121 12.9446C1.43774 13.0303 1.63821 13.0157 1.79062 12.9069L1.5 12.5ZM8.5 7.5L8.79062 7.90687C8.92202 7.81301 9 7.66148 9 7.5C9 7.33852 8.92202 7.18699 8.79062 7.09313L8.5 7.5ZM1 2.5V12.5H2V2.5H1ZM1.79062 12.9069L8.79062 7.90687L8.20938 7.09313L1.20938 12.0931L1.79062 12.9069ZM8.79062 7.09313L1.79062 2.09313L1.20938 2.90687L8.20938 7.90687L8.79062 7.09313ZM13 2V13H14V2H13Z" fill="${color}"/> `;
  let svgsolid = `<path d="M1.79062 2.09314C1.63821 1.98427 1.43774 1.96972 1.27121 2.05542C1.10467 2.14112 1 2.31271 1 2.5V12.5C1 12.6873 1.10467 12.8589 1.27121 12.9446C1.43774 13.0303 1.63821 13.0157 1.79062 12.9069L8.79062 7.90687C8.92202 7.81301 9 7.66148 9 7.5C9 7.33853 8.92202 7.18699 8.79062 7.09314L1.79062 2.09314Z" fill="${color}"/> <path d="M13 13H14V2H13V13Z" fill="${color}"/> `;
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
  export let ariaLabel = 'next';
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
