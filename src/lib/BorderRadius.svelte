<script lang="ts">
  export let size: string = '15';
  export let color: string = 'black';
  export let variation: 'solid' | 'outline' = 'outline';
  let svgpath: string;
  let svgoutline = `<path d="M10 1.5H11M13 1.5H14M13 4.5H14M13 7.5H14M13 10.5H14M13 13.5H14M10 13.5H11M7 13.5H8M4 13.5H5M1 13.5H2M1 10.5H2M1.5 8V5.5C1.5 3.29086 3.29086 1.5 5.5 1.5H8" stroke="${color}"/> `;
  let svgsolid = `<path fill-rule="evenodd" clip-rule="evenodd" d="M5.5 2C3.567 2 2 3.567 2 5.5V8H1V5.5C1 3.01472 3.01472 1 5.5 1H8V2H5.5ZM11 2H10V1H11V2ZM14 2H13V1H14V2ZM14 5H13V4H14V5ZM14 8H13V7H14V8ZM2 11H1V10H2V11ZM14 11H13V10H14V11ZM2 14H1V13H2V14ZM5 14H4V13H5V14ZM8 14H7V13H8V14ZM11 14H10V13H11V14ZM14 14H13V13H14V14Z" fill="${color}"/> `;
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
  export let ariaLabel = 'border radius';
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
