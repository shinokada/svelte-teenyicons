<script lang="ts">
  export let size: string = '15';
  export let color: string = 'black';
  export let variation: 'solid' | 'outline' = 'outline';
  let svgpath: string;
  let svgoutline = `<path d="M6 11.5H9M3.5 14.5H11.5C12.0523 14.5 12.5 14.0523 12.5 13.5V1.5C12.5 0.947715 12.0523 0.5 11.5 0.5H3.5C2.94772 0.5 2.5 0.947716 2.5 1.5V13.5C2.5 14.0523 2.94772 14.5 3.5 14.5Z" stroke="${color}"/> `;
  let svgsolid = `<path fill-rule="evenodd" clip-rule="evenodd" d="M2 1.5C2 0.671573 2.67157 0 3.5 0H11.5C12.3284 0 13 0.671573 13 1.5V13.5C13 14.3284 12.3284 15 11.5 15H3.5C2.67157 15 2 14.3284 2 13.5V1.5ZM6 12H9V11H6V12Z" fill="${color}"/> `;
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
  export let ariaLabel = 'mobile';
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
