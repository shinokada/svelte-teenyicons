<script lang="ts">
	export let size: string = '15';
	export let color: string = 'black';
	export let variation: 'solid' | 'outline' = 'outline';
	let svgpath: string;
	let svgoutline = `<path d="M3.5 0V5M11.5 0V5M5 8.5H10M1.5 2.5H13.5C14.0523 2.5 14.5 2.94772 14.5 3.5V13.5C14.5 14.0523 14.0523 14.5 13.5 14.5H1.5C0.947716 14.5 0.5 14.0523 0.5 13.5V3.5C0.5 2.94772 0.947715 2.5 1.5 2.5Z" stroke="${color}"/> `;
	let svgsolid = `<path fill-rule="evenodd" clip-rule="evenodd" d="M13.5 2H12V0H11V2H4V0H3V2H1.5C0.671573 2 0 2.67157 0 3.5V13.5C0 14.3284 0.671573 15 1.5 15H13.5C14.3284 15 15 14.3284 15 13.5V3.5C15 2.67157 14.3284 2 13.5 2ZM5 9H10V8H5V9Z" fill="${color}"/> `;
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
	export let ariaLabel = 'calendar minus';
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
