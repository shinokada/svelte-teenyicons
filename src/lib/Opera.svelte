<script lang="ts">
  export let size: string = "15";
  export let color: string = "black" 
  export let variation: "solid" | "outline" = "outline";
  let svgpath: string;
  let svgoutline = `<path d="M7.5 12.5C5.84315 12.5 4.5 11.1569 4.5 9.5V5.5C4.5 3.84315 5.84315 2.5 7.5 2.5M7.5 12.5C9.15685 12.5 10.5 11.1569 10.5 9.5V5.5C10.5 3.84315 9.15685 2.5 7.5 2.5M7.5 12.5H8.08452C9.99226 12.5 11.8641 11.9815 13.5 11M7.5 2.5H8.08452C9.99226 2.5 11.8641 3.01848 13.5 4M7.5 14.5C3.63401 14.5 0.5 11.366 0.5 7.5C0.5 3.63401 3.63401 0.5 7.5 0.5C11.366 0.5 14.5 3.63401 14.5 7.5C14.5 11.366 11.366 14.5 7.5 14.5Z" stroke="${color}"/> `;
  let svgsolid = `<path d="M0 7.5C0 3.35786 3.35786 0 7.5 0C9.75175 0 11.7717 0.992326 13.1465 2.56352C11.7095 2.18977 10.2292 2 8.74128 2H7.5C5.567 2 4 3.567 4 5.5V9.5C4 11.433 5.567 13 7.5 13L8.74128 13C10.2292 13 11.7095 12.8102 13.1465 12.4365C11.7717 14.0077 9.75174 15 7.5 15C3.35786 15 0 11.6421 0 7.5Z" fill="${color}"/> <path d="M14.0726 11.1154C14.6637 10.0432 15 8.81088 15 7.5C15 6.18913 14.6637 4.9568 14.0727 3.8846L13.959 3.84673C12.6747 3.41862 11.3441 3.15071 9.99743 3.04788C10.6175 3.67938 11 4.54503 11 5.5V9.5C11 10.455 10.6175 11.3206 9.99742 11.9521C11.3441 11.8493 12.6747 11.5814 13.959 11.1533L14.0726 11.1154Z" fill="${color}"/> `;
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
export let ariaLabel="opera" </script>

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
