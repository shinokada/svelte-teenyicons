<script lang="ts">
	export let size = '15';
	export let variation: 'solid' | 'outline' = 'outline';
	let svgpath: string;
	let svgoutline = `<path d="M1.5 9.5H2.5C3.05228 9.5 3.5 9.94772 3.5 10.5V13.5C3.5 14.0523 3.05228 14.5 2.5 14.5H1.5C0.947715 14.5 0.5 14.0523 0.5 13.5V10.5C0.5 9.94772 0.947715 9.5 1.5 9.5ZM1.5 9.5V6.5C1.5 3.18629 4.18629 0.5 7.5 0.5C10.8137 0.5 13.5 3.18629 13.5 6.5V9.5M13.5 9.5H12.5C11.9477 9.5 11.5 9.94772 11.5 10.5V13.5C11.5 14.0523 11.9477 14.5 12.5 14.5H13.5C14.0523 14.5 14.5 14.0523 14.5 13.5V10.5C14.5 9.94772 14.0523 9.5 13.5 9.5Z" stroke="black"/> `;
	let svgsolid = `<path d="M2 6.5C2 3.46243 4.46243 1 7.5 1C10.5376 1 13 3.46243 13 6.5V9H12.5C11.6716 9 11 9.67157 11 10.5V13.5C11 14.3284 11.6716 15 12.5 15H13.5C14.3284 15 15 14.3284 15 13.5V10.5C15 9.84689 14.5826 9.29127 14 9.08535V6.5C14 2.91015 11.0899 0 7.5 0C3.91015 0 1 2.91015 1 6.5V9.08535C0.417404 9.29127 0 9.84689 0 10.5V13.5C0 14.3284 0.671573 15 1.5 15H2.5C3.32843 15 4 14.3284 4 13.5V10.5C4 9.67157 3.32843 9 2.5 9H2V6.5Z" fill="black"/> `;
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
	export let ariaLabel = 'headphones';
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
