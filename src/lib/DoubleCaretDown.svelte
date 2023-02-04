<script lang="ts">
  export let size: string = '15';
  export let color: string = 'black';
  export let variation: 'solid' | 'outline' = 'outline';
  let svgpath: string;
  let svgoutline = `<path d="M1 7L7.5 14L14 7M1 1.5L7.5 8.5L14 1.5" stroke="${color}" stroke-linecap="square"/> `;
  let svgsolid = `<path fill-rule="evenodd" clip-rule="evenodd" d="M14.7066 1.47385L7.5 9.23483L0.293375 1.47385L1.02617 0.793396L7.5 7.76521L13.9738 0.793396L14.7066 1.47385ZM1.02617 6.2934L7.5 13.2652L13.9738 6.2934L14.7066 6.97385L7.5 14.7348L0.293375 6.97385L1.02617 6.2934Z" fill="${color}"/> `;
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
  export let ariaLabel = 'double caret down';
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
