<script lang="ts">
  export let size: string = '15';
  export let color: string = 'black';
  export let variation: 'solid' | 'outline' = 'outline';
  let svgpath: string;
  let svgoutline = `<path d="M0.5 3.5L3.5 0.5M11.5 0.5L14.5 3.5M7.5 5V8.5H10M7.5 2.5C4.18629 2.5 1.5 5.18629 1.5 8.5C1.5 11.8137 4.18629 14.5 7.5 14.5C10.8137 14.5 13.5 11.8137 13.5 8.5C13.5 5.18629 10.8137 2.5 7.5 2.5Z" stroke="${color}"/> `;
  let svgsolid = `<path d="M3.85359 0.853591L0.853591 3.85359L0.146484 3.14648L3.14648 0.146484L3.85359 0.853591Z" fill="${color}"/> <path d="M14.1465 3.85359L11.1465 0.853591L11.8536 0.146484L14.8536 3.14648L14.1465 3.85359Z" fill="${color}"/> <path fill-rule="evenodd" clip-rule="evenodd" d="M1 8.50003C1 4.91018 3.91015 2.00003 7.5 2.00003C11.0899 2.00003 14 4.91018 14 8.50003C14 12.0899 11.0899 15 7.5 15C3.91015 15 1 12.0899 1 8.50003ZM8 8.00003V5.00003H7V9.00003H10V8.00003H8Z" fill="${color}"/> `;
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
  export let ariaLabel = 'alarm';
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
