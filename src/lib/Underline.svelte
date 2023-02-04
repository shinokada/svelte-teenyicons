<script lang="ts">
  export let size: string = '15';
  export let color: string = 'black';
  export let variation: 'solid' | 'outline' = 'outline';
  let svgpath: string;
  let svgoutline = `<path d="M2 13.5H13M3.5 1V7.5C3.5 9.70914 5.29086 11.5 7.5 11.5C9.70914 11.5 11.5 9.70914 11.5 7.5V1" stroke="${color}"/> `;
  let svgsolid = `<path fill-rule="evenodd" clip-rule="evenodd" d="M3 7.5V1H4V7.5C4 9.433 5.567 11 7.5 11C9.433 11 11 9.433 11 7.5V1H12V7.5C12 9.98528 9.98528 12 7.5 12C5.01472 12 3 9.98528 3 7.5ZM13 13V14H2V13H13Z" fill="${color}"/> `;
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
  export let ariaLabel = 'underline';
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
