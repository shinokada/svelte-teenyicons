<script lang="ts">
  export let size: string = '15';
  export let color: string = 'black';
  export let variation: 'solid' | 'outline' = 'outline';
  let svgpath: string;
  let svgoutline = `<path d="M3 11.5H0.5V1.5H14.5V11.5H12M7.5 9.5L3.5 13.5H11.5L7.5 9.5Z" stroke="${color}" stroke-linejoin="round"/> `;
  let svgsolid = `<path d="M0.5 1C0.223858 1 0 1.22386 0 1.5V11.5C0 11.7761 0.223858 12 0.5 12H3V11H1V2H14V11H12V12H14.5C14.7761 12 15 11.7761 15 11.5V1.5C15 1.22386 14.7761 1 14.5 1H0.5Z" fill="${color}"/> <path d="M7.85355 9.14645C7.65829 8.95118 7.34171 8.95118 7.14645 9.14645L3.14645 13.1464C3.00345 13.2894 2.96067 13.5045 3.03806 13.6913C3.11545 13.8782 3.29777 14 3.5 14H11.5C11.7022 14 11.8845 13.8782 11.9619 13.6913C12.0393 13.5045 11.9966 13.2894 11.8536 13.1464L7.85355 9.14645Z" fill="${color}"/> `;
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
  export let ariaLabel = 'airplay';
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
