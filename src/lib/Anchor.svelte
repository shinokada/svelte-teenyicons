<script lang="ts">
  export let size: string = "15";
  export let color: string = "black" 
  export let variation: "solid" | "outline" = "outline";
  let svgpath: string;
  let svgoutline = `<path d="M7.5 4.49744C8.604 4.49744 9.5 3.60206 9.5 2.49878C9.5 1.39549 8.604 0.5 7.5 0.5C6.396 0.5 5.5 1.39549 5.5 2.49878C5.5 3.60206 6.396 4.49744 7.5 4.49744ZM7.5 4.49744V14.4908M7.5 14.4908C3.634 14.4908 0.5 11.359 0.5 7.49548H2.5M7.5 14.4908C11.366 14.4908 14.5 11.359 14.5 7.49548H12.5" stroke="${color}" stroke-linecap="square"/> `;
  let svgsolid = `<path fill-rule="evenodd" clip-rule="evenodd" d="M7.5 1C6.67186 1 6 1.67191 6 2.49878C6 3.3256 6.67182 3.99744 7.5 3.99744C8.32818 3.99744 9 3.3256 9 2.49878C9 1.67191 8.32814 1 7.5 1ZM5 2.49878C5 1.11907 6.12014 0 7.5 0C8.87986 0 10 1.11907 10 2.49878C10 3.70732 9.14056 4.71574 8 4.94739V13.9719C11.1913 13.7293 13.7381 11.184 13.981 7.99548H12V6.99548H15V7.49548C15 11.6354 11.6418 14.9908 7.5 14.9908C3.35817 14.9908 0 11.6354 0 7.49548V6.99548H3V7.99548H1.01897C1.26189 11.184 3.80867 13.7293 7 13.9719V4.94739C5.85944 4.71574 5 3.70732 5 2.49878Z" fill="${color}"/> `;
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
export let ariaLabel="anchor" </script>

<svg
  xmlns="http://www.w3.org/2000/svg"
  width={size}
  height={size}
  fill="none"
  class={$$props.class}
  {...$$restProps}
  aria-label={ariaLabel}
  viewBox="0 0 15 15"
  on:click 
  on:mouseenter 
  on:mouseleave 
  on:mouseover 
  on:mouseout 
  on:blur 
  on:focus 
>
  {@html svgpath}
</svg>
