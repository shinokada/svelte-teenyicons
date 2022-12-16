<script lang="ts">
  export let size: string = '15';
  export let color: string = 'black';
  export let variation: 'solid' | 'outline' = 'outline';
  let svgpath: string;
  let svgoutline = `<path d="M4 7.5L7 10L11 5" stroke="${color}"/> `;
  let svgsolid = `<path fill-rule="evenodd" clip-rule="evenodd" d="M11.3904 5.31232L7.07178 10.7106L3.67991 7.88408L4.32009 7.11586L6.92822 9.2893L10.6096 4.68762L11.3904 5.31232Z" fill="${color}"/> `;
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
  export let ariaLabel = 'tick small';
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
