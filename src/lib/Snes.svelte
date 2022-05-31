<script lang="ts">
	export let size = '15';
	export let ariaLabel = '360';
	export let variation: 'solid' | 'outline' = 'outline';
	let svgpath: string;
	let svgoutline = `<path d="M3.5 7V10M2 8.5H5M11 8.5H12M11 6.5H12M9 8.5H10M9 6.5H10M1.5 3.5H13.5C14.0523 3.5 14.5 3.94772 14.5 4.5V10.5C14.5 11.0523 14.0523 11.5 13.5 11.5H1.5C0.947716 11.5 0.5 11.0523 0.5 10.5V4.5C0.5 3.94772 0.947715 3.5 1.5 3.5Z" stroke="black"/> `;
	let svgsolid = `<path fill-rule="evenodd" clip-rule="evenodd" d="M0 4.5C0 3.67157 0.671573 3 1.5 3H13.5C14.3284 3 15 3.67157 15 4.5V10.5C15 11.3284 14.3284 12 13.5 12H1.5C0.671573 12 0 11.3284 0 10.5V4.5ZM12 7H11V6H12V7ZM3 10V9H2V8H3V7H4V8H5V9H4V10H3ZM11 9H12V8H11V9ZM9 9H10V8H9V9ZM10 7H9V6H10V7Z" fill="black"/> `;
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
