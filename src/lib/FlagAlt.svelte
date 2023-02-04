<script lang="ts">
  export let size: string = '15';
  export let color: string = 'black';
  export let variation: 'solid' | 'outline' = 'outline';
  let svgpath: string;
  let svgoutline = `<path d="M12.5 6.5L12.7236 6.94721C12.8868 6.8656 12.9926 6.70154 12.9996 6.51919C13.0066 6.33683 12.9137 6.16514 12.7572 6.07125L12.5 6.5ZM2.5 0.5L2.75725 0.0712535C2.60278 -0.0214257 2.4104 -0.0238528 2.25365 0.0649C2.0969 0.153653 2 0.319864 2 0.5L2.5 0.5ZM12.7572 6.07125L2.75725 0.0712535L2.24275 0.928746L12.2428 6.92875L12.7572 6.07125ZM2 0.5V11.5H3V0.5H2ZM2.72361 11.9472L12.7236 6.94721L12.2764 6.05279L2.27639 11.0528L2.72361 11.9472ZM3 15V11.5H2V15H3Z" fill="${color}"/> `;
  let svgsolid = `<path d="M2.25365 0.0649001C2.4104 -0.0238527 2.60278 -0.0214256 2.75725 0.0712536L12.7572 6.07125C12.9137 6.16514 13.0066 6.33683 12.9996 6.51919C12.9926 6.70154 12.8868 6.8656 12.7236 6.94721L3 11.809V15H2V0.5C2 0.319864 2.0969 0.153653 2.25365 0.0649001Z" fill="${color}"/> `;
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
  export let ariaLabel = 'flag alt';
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
