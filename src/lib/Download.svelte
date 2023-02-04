<script lang="ts">
  export let size: string = '15';
  export let color: string = 'black';
  export let variation: 'solid' | 'outline' = 'outline';
  let svgpath: string;
  let svgoutline = `<path d="M7.5 10.5L4.25 7.5M7.5 10.5L10.5 7.5M7.5 10.5V1M13.5 7V13.5H1.5V7" stroke="${color}"/> `;
  let svgsolid = `<path fill-rule="evenodd" clip-rule="evenodd" d="M7 9.35801V1H8V9.29289L10.1464 7.14645L10.8536 7.85355L7.51386 11.1932L3.91086 7.8674L4.58914 7.1326L7 9.35801ZM2 13V7H1V14H14V7H13V13H2Z" fill="${color}"/> `;
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
  export let ariaLabel = 'download';
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
