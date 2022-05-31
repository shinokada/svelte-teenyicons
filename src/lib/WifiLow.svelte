<script lang="ts">
  export let size = "15";
  export let ariaLabel = "360";
  export let variation: "solid" | "outline" = "outline";
  let svgpath: string;
  let svgoutline = `<path d="M3.21907 9.31819C4.37371 7.91855 5.91677 7.15686 7.50004 7.15686V6.15686C5.58264 6.15686 3.76839 7.08088 2.44768 8.68182L3.21907 9.31819ZM7.50004 7.15686C9.08331 7.15686 10.6264 7.91855 11.781 9.31819L12.5524 8.68182C11.2317 7.08088 9.41745 6.15686 7.50004 6.15686V7.15686ZM7.5 12C7.22386 12 7 11.7761 7 11.5H6C6 12.3284 6.67157 13 7.5 13V12ZM8 11.5C8 11.7761 7.77614 12 7.5 12V13C8.32843 13 9 12.3284 9 11.5H8ZM7.5 11C7.77614 11 8 11.2239 8 11.5H9C9 10.6716 8.32843 10 7.5 10V11ZM7.5 10C6.67157 10 6 10.6716 6 11.5H7C7 11.2239 7.22386 11 7.5 11V10Z" fill="black"/> `;
  let svgsolid = `<path d="M3.2189 9.31819C4.37354 7.91855 5.9166 7.15686 7.49987 7.15686C9.08314 7.15686 10.6262 7.91855 11.7808 9.31819L12.5522 8.68182C11.2315 7.08088 9.41728 6.15686 7.49987 6.15686C5.58247 6.15686 3.76822 7.08088 2.44751 8.68182L3.2189 9.31819Z" fill="black"/> <path d="M6 11.5C6 10.6716 6.67157 10 7.5 10C8.32843 10 9 10.6716 9 11.5C9 12.3284 8.32843 13 7.5 13C6.67157 13 6 12.3284 6 11.5Z" fill="black"/> `;
  switch (variation) {
    case "outline":
      svgpath = svgoutline;
      break;
    case "solid":
      svgpath = svgsolid;
      break;
    default:
      svgpath = svgoutline;
  }
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
