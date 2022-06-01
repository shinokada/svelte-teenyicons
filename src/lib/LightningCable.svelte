<script lang="ts">
	export let size = '15';
	export let variation: 'solid' | 'outline' = 'outline';
	let svgpath: string;
	let svgoutline = `<path d="M4.5 5.5H10.5M4.5 5.5C3.94772 5.5 3.5 5.94772 3.5 6.5V11.5C3.5 12.0523 3.94772 12.5 4.5 12.5H10.5C11.0523 12.5 11.5 12.0523 11.5 11.5V6.5C11.5 5.94772 11.0523 5.5 10.5 5.5M4.5 5.5V1.5C4.5 0.947715 4.94772 0.5 5.5 0.5H9.5C10.0523 0.5 10.5 0.947715 10.5 1.5V5.5M9 2.5H6M5.5 13V15M9.5 13V15" stroke="black"/> `;
	let svgsolid = `<path fill-rule="evenodd" clip-rule="evenodd" d="M5.5 0C4.67157 0 4 0.671573 4 1.5V5H11V1.5C11 0.671573 10.3284 0 9.5 0H5.5ZM6 2H9V3H6V2Z" fill="black"/> <path d="M3 6H12V11.5C12 12.3284 11.3284 13 10.5 13L10 13V15H9V13H6V15H5V13L4.5 13C3.67157 13 3 12.3284 3 11.5V6Z" fill="black"/> `;
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
	export let ariaLabel = 'lightning cable';
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
