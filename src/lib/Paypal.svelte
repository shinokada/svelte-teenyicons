<script lang="ts">
  export let size = "15";
  export let ariaLabel = "360";
  export let variation: "solid" | "outline" = "outline";
  let svgpath: string;
  let svgoutline = `<path d="M0.5 12.5H4.5L5.5 8.5H7.29496C9.22281 8.5 10.9485 7.30413 11.6254 5.49902C12.5324 3.08021 10.7443 0.5 8.16104 0.5H3.5L0.5 12.5Z" stroke="black" stroke-linejoin="round"/> <path d="M4 14.5H8L9 11H10.5767C12.054 11 13.3964 10.141 14.0155 8.7997C14.9422 6.79198 13.4757 4.5 11.2644 4.5H6.5L4 14.5Z" stroke="black" stroke-linejoin="round"/> `;
  let svgsolid = `<path fill-rule="evenodd" clip-rule="evenodd" d="M3.01493 0.378732C3.07058 0.156149 3.27057 0 3.5 0H8.16104C10.5583 0 12.3523 1.95748 12.3647 4.17206C14.2927 4.79825 15.3862 7.02313 14.4695 9.00923C13.7687 10.5276 12.249 11.5 10.5767 11.5H9.37716L8.48077 14.6374C8.41944 14.852 8.22325 15 8 15H4C3.84604 15 3.70066 14.9291 3.6059 14.8077C3.51115 14.6863 3.47759 14.5281 3.51493 14.3787L3.85962 13H0.500005C0.346037 13 0.200655 12.9291 0.105902 12.8077C0.0111482 12.6863 -0.0224094 12.5281 0.0149333 12.3787L3.01493 0.378732ZM8.16104 1C9.92319 1 11.2575 2.38818 11.3578 4.00117C11.3268 4.00039 11.2957 4 11.2644 4H6.5C6.27057 4 6.07058 4.15615 6.01493 4.37873L4.10962 12H1.14039L3.89039 1H8.16104ZM7.29496 9H5.89039L4.64039 14H7.62285L8.51924 10.8626C8.58057 10.648 8.77676 10.5 9 10.5H10.5767C11.8589 10.5 13.0242 9.75443 13.5615 8.59018C14.1878 7.23324 13.5049 5.72079 12.2427 5.19362C12.2031 5.35415 12.1535 5.51468 12.0935 5.67459C11.3434 7.67485 9.43124 9 7.29496 9Z" fill="black"/> `;
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
