<script lang="ts">
	export let size = '15';
	export let variation: 'solid' | 'outline' = 'outline';
	let svgpath: string;
	let svgoutline = `<path d="M1.5 6.5H5.5C6.05228 6.5 6.5 6.05228 6.5 5.5V2.5C6.5 1.94772 6.05228 1.5 5.5 1.5H2.5C1.94772 1.5 1.5 1.94772 1.5 2.5V6.5ZM1.5 6.5V10C1.5 11.933 3.067 13.5 5 13.5M8.5 6.5H12.5C13.0523 6.5 13.5 6.05228 13.5 5.5V2.5C13.5 1.94772 13.0523 1.5 12.5 1.5H9.5C8.94772 1.5 8.5 1.94772 8.5 2.5V6.5ZM8.5 6.5V10C8.5 11.933 10.067 13.5 12 13.5" stroke="black"/> `;
	let svgsolid = `<path d="M2.5 1C1.67157 1 1 1.67157 1 2.5V10C1 12.2091 2.79086 14 5 14V13C3.34315 13 2 11.6569 2 10V7H5.5C6.32843 7 7 6.32843 7 5.5V2.5C7 1.67157 6.32843 1 5.5 1H2.5Z" fill="black"/> <path d="M9.5 1C8.67157 1 8 1.67157 8 2.5V10C8 12.2091 9.79086 14 12 14V13C10.3431 13 9 11.6569 9 10V7H12.5C13.3284 7 14 6.32843 14 5.5V2.5C14 1.67157 13.3284 1 12.5 1H9.5Z" fill="black"/> `;
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
	export let ariaLabel = 'quote';
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
