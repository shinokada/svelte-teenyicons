<script lang="ts">
  export let size: string = '15';
  export let color: string = 'black';
  export let variation: 'solid' | 'outline' = 'outline';
  let svgpath: string;
  let svgoutline = `<path d="M8.14645 9.14645L7.79289 9.5L8.5 10.2071L8.85355 9.85355L8.14645 9.14645ZM10.5 7.5L10.8536 7.85355L11.2071 7.5L10.8536 7.14645L10.5 7.5ZM8.85355 5.14645L8.5 4.79289L7.79289 5.5L8.14645 5.85355L8.85355 5.14645ZM8.85355 9.85355L10.8536 7.85355L10.1464 7.14645L8.14645 9.14645L8.85355 9.85355ZM10.8536 7.14645L8.85355 5.14645L8.14645 5.85355L10.1464 7.85355L10.8536 7.14645ZM10.5 7H4V8H10.5V7ZM7.5 14C3.91015 14 1 11.0899 1 7.5H0C0 11.6421 3.35786 15 7.5 15V14ZM14 7.5C14 11.0899 11.0899 14 7.5 14V15C11.6421 15 15 11.6421 15 7.5H14ZM7.5 1C11.0899 1 14 3.91015 14 7.5H15C15 3.35786 11.6421 0 7.5 0V1ZM7.5 0C3.35786 0 0 3.35786 0 7.5H1C1 3.91015 3.91015 1 7.5 1V0Z" fill="${color}"/> `;
  let svgsolid = `<path fill-rule="evenodd" clip-rule="evenodd" d="M0 7.5C0 3.35786 3.35786 0 7.5 0C11.6421 0 15 3.35786 15 7.5C15 11.6421 11.6421 15 7.5 15C3.35786 15 0 11.6421 0 7.5ZM8.50008 4.79285L11.2072 7.49995L8.50008 10.2071L7.79297 9.49995L9.29292 8H4V7H9.29302L7.79297 5.49995L8.50008 4.79285Z" fill="${color}"/> `;
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
  export let ariaLabel = 'arrow right circle';
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
