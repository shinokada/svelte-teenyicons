<script lang="ts">
	export let size = '15';
	export let variation: 'solid' | 'outline' = 'outline';
	let svgpath: string;
	let svgoutline = `<path d="M5 8.5H10M0.5 0.5H14.5V4.5H0.5V0.5ZM1.5 4.5V13.5C1.5 14.0523 1.94772 14.5 2.5 14.5H12.5C13.0523 14.5 13.5 14.0523 13.5 13.5V4.5H1.5Z" stroke="black"/> `;
	let svgsolid = `<path d="M0 0H15V5H0V0Z" fill="black"/> <path fill-rule="evenodd" clip-rule="evenodd" d="M1 6V13.5C1 14.3284 1.67157 15 2.5 15H12.5C13.3284 15 14 14.3284 14 13.5V6H1ZM10 9H5V8H10V9Z" fill="black"/> `;
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
	export let ariaLabel = 'archive';
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
