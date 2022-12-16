<script lang="ts">
  export let size: string = '15';
  export let color: string = 'black';
  export let variation: 'solid' | 'outline' = 'outline';
  let svgpath: string;
  let svgoutline = `<path d="M7.5 15V7.5M7.5 7.5L2.5 0.5M7.5 7.5L12.5 0.5M3 7.5H12M3 11.5H12" stroke="${color}"/> `;
  let svgsolid = `<path fill-rule="evenodd" clip-rule="evenodd" d="M6.52841 7H3.00001V8H7.00001V11H3.00001V12H7.00001V15H8.00001V12H12V11H8.00001V8H12V7H8.4716L12.9069 0.790619L12.0931 0.209381L7.50001 6.63977L2.90687 0.209381L2.09314 0.790619L6.52841 7Z" fill="${color}"/> `;
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
  export let ariaLabel = 'yen';
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
