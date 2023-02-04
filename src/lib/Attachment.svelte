<script lang="ts">
  export let size: string = '15';
  export let color: string = 'black';
  export let variation: 'solid' | 'outline' = 'outline';
  let svgpath: string;
  let svgoutline = `<path d="M0.5 0V4.5C0.5 5.60457 1.39543 6.5 2.5 6.5C3.60457 6.5 4.5 5.60457 4.5 4.5V1.5C4.5 0.947715 4.05228 0.5 3.5 0.5C2.94772 0.5 2.5 0.947715 2.5 1.5V5M6 0.5H12.5C13.0523 0.5 13.5 0.947715 13.5 1.5V13.5C13.5 14.0523 13.0523 14.5 12.5 14.5H2.5C1.94772 14.5 1.5 14.0523 1.5 13.5V8M11 4.5H7M11 7.5H7M11 10.5H4" stroke="${color}"/> `;
  let svgsolid = `<path d="M0 4.5V0H1V4.5C1 5.32843 1.67157 6 2.5 6C3.32843 6 4 5.32843 4 4.5V1.5C4 1.22386 3.77614 1 3.5 1C3.22386 1 3 1.22386 3 1.5V5H2V1.5C2 0.671573 2.67157 0 3.5 0C4.32843 0 5 0.671573 5 1.5V4.5C5 5.88071 3.88071 7 2.5 7C1.11929 7 0 5.88071 0 4.5Z" fill="${color}"/> <path fill-rule="evenodd" clip-rule="evenodd" d="M12.5 0H6V4.5C6 6.433 4.433 8 2.5 8H1V13.5C1 14.3284 1.67157 15 2.5 15H12.5C13.3284 15 14 14.3284 14 13.5V1.5C14 0.671573 13.3284 0 12.5 0ZM11 4H7V5H11V4ZM11 7H7V8H11V7ZM4 10H11V11H4V10Z" fill="${color}"/> `;
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
  export let ariaLabel = 'attachment';
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
