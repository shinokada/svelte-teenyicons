<script lang="ts">
  export let size: string = '15';
  export let color: string = 'black';
  export let variation: 'solid' | 'outline' = 'outline';
  let svgpath: string;
  let svgoutline = `<path d="M4.5 7.5V7C4.36739 7 4.24021 7.05268 4.14645 7.14645C4.05268 7.24021 4 7.36739 4 7.5H4.5ZM10.5 7.5H11C11 7.36739 10.9473 7.24021 10.8536 7.14645C10.7598 7.05268 10.6326 7 10.5 7V7.5ZM10.5 7H4.5V8H10.5V7ZM7.5 11C9.47066 11 11 9.47066 11 7.5H10C10 8.91838 8.91838 10 7.5 10V11ZM4 7.5C4 9.47066 5.52934 11 7.5 11V10C6.08162 10 5 8.91838 5 7.5H4ZM7.5 14C3.91015 14 1 11.0899 1 7.5H0C0 11.6421 3.35786 15 7.5 15V14ZM14 7.5C14 11.0899 11.0899 14 7.5 14V15C11.6421 15 15 11.6421 15 7.5H14ZM7.5 1C11.0899 1 14 3.91015 14 7.5H15C15 3.35786 11.6421 0 7.5 0V1ZM7.5 0C3.35786 0 0 3.35786 0 7.5H1C1 3.91015 3.91015 1 7.5 1V0ZM4 6H5V5H4V6ZM10 6H11V5H10V6Z" fill="${color}"/> `;
  let svgsolid = `<path d="M7.5 10C6.25369 10 5.26738 9.16489 5.04642 8H9.95358C9.73262 9.16489 8.74631 10 7.5 10Z" fill="${color}"/> <path fill-rule="evenodd" clip-rule="evenodd" d="M0 7.5C0 3.35786 3.35786 0 7.5 0C11.6421 0 15 3.35786 15 7.5C15 11.6421 11.6421 15 7.5 15C3.35786 15 0 11.6421 0 7.5ZM4 6H5V5H4V6ZM4.5 7C4.36739 7 4.24021 7.05268 4.14645 7.14645C4.05268 7.24021 4 7.36739 4 7.5C4 9.47066 5.52934 11 7.5 11C9.47066 11 11 9.47066 11 7.5C11 7.36739 10.9473 7.24021 10.8536 7.14645C10.7598 7.05268 10.6326 7 10.5 7H4.5ZM11 6H10V5H11V6Z" fill="${color}"/> `;
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
  export let ariaLabel = 'mood laugh';
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
