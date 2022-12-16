<script lang="ts">
	export let size: string = '15';
	export let color: string = 'black';
	export let variation: 'solid' | 'outline' = 'outline';
	let svgpath: string;
	let svgoutline = `<path d="M4 4.5H11M4 8.5H5M7 8.5H8M10 8.5H11M4 11.5H5M7 11.5H8M10 11.5H11M2.5 14.5H12.5C13.0523 14.5 13.5 14.0523 13.5 13.5V1.5C13.5 0.947715 13.0523 0.5 12.5 0.5H2.5C1.94772 0.5 1.5 0.947716 1.5 1.5V13.5C1.5 14.0523 1.94772 14.5 2.5 14.5Z" stroke="${color}"/> `;
	let svgsolid = `<path fill-rule="evenodd" clip-rule="evenodd" d="M1 1.5C1 0.671573 1.67157 0 2.5 0H12.5C13.3284 0 14 0.671573 14 1.5V13.5C14 14.3284 13.3284 15 12.5 15H2.5C1.67157 15 1 14.3284 1 13.5V1.5ZM4 5H11V4H4V5ZM4 9H5V8H4V9ZM8 9H7V8H8V9ZM10 9H11V8H10V9ZM5 12H4V11H5V12ZM7 12H8V11H7V12ZM11 12H10V11H11V12Z" fill="${color}"/> `;
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
	export let ariaLabel = 'calculator';
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
