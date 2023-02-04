<script lang="ts">
  export let size: string = '15';
  export let color: string = 'black';
  export let variation: 'solid' | 'outline' = 'outline';
  let svgpath: string;
  let svgoutline = `<path d="M10 5.5L9.93198 5.43198C9.33524 4.83524 8.52589 4.5 7.68198 4.5H7.5C5.84315 4.5 4.5 5.84315 4.5 7.5C4.5 9.15685 5.84315 10.5 7.5 10.5H7.68198C8.52589 10.5 9.33524 10.1648 9.93198 9.56802L10 9.5M1.5 10.5V4.5L7.5 1L13.5 4.5V10.5L7.5 14L1.5 10.5Z" stroke="${color}"/> `;
  let svgsolid = `<path fill-rule="evenodd" clip-rule="evenodd" d="M7.5 0.421143L14 4.21281V10.7872L7.5 14.5788L1 10.7872V4.21281L7.5 0.421143ZM7.5 4C5.567 4 4 5.567 4 7.5C4 9.433 5.567 11 7.5 11H7.68198C8.6585 11 9.59503 10.6121 10.2855 9.92157L10.3536 9.85355L9.64645 9.14645L9.57843 9.21447C9.07546 9.71744 8.39329 10 7.68198 10H7.5C6.11929 10 5 8.88071 5 7.5C5 6.11929 6.11929 5 7.5 5H7.68198C8.39329 5 9.07546 5.28257 9.57843 5.78553L9.64645 5.85355L10.3536 5.14645L10.2855 5.07843C9.59503 4.38792 8.6585 4 7.68198 4H7.5Z" fill="${color}"/> `;
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
  export let ariaLabel = 'c';
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
