<script lang="ts">
	export let size: string = '15';
	export let color: string = 'black';
	export let variation: 'solid' | 'outline' = 'outline';
	let svgpath: string;
	let svgoutline = `<path d="M4.49998 4V3.5C4.49998 1.84315 5.84313 0.5 7.49998 0.5C9.15683 0.5 10.5 1.84315 10.5 3.5V4M4.99998 9.5H9.99998M2.40114 6.38957L1.62336 13.3896C1.55754 13.9819 2.02123 14.5 2.61724 14.5H12.3827C12.9787 14.5 13.4424 13.9819 13.3766 13.3896L12.5988 6.38957C12.5426 5.88313 12.1145 5.5 11.6049 5.5H3.39502C2.88547 5.5 2.45741 5.88314 2.40114 6.38957Z" stroke="${color}"/> `;
	let svgsolid = `<path d="M7.5 1C6.11929 1 5 2.11929 5 3.5V4H4V3.5C4 1.567 5.567 0 7.5 0C9.433 0 11 1.567 11 3.5V4H10V3.5C10 2.11929 8.88071 1 7.5 1Z" fill="${color}"/> <path fill-rule="evenodd" clip-rule="evenodd" d="M3.39514 5C2.63082 5 1.98872 5.5747 1.90432 6.33435L1.12654 13.3344C1.02781 14.2229 1.72335 15 2.61737 15H12.3828C13.2769 15 13.9724 14.2229 13.8737 13.3344L13.0959 6.33435C13.0115 5.5747 12.3694 5 11.6051 5H3.39514ZM5 9V10H10V9H5Z" fill="${color}"/> `;
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
	export let ariaLabel = 'bag minus';
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
