<script lang="ts">
	export let size = '15';
	export let variation: 'solid' | 'outline' = 'outline';
	let svgpath: string;
	let svgoutline = `<path d="M13.5 0.5H1.5C0.947715 0.5 0.5 0.947716 0.5 1.5V13.5C0.5 14.0523 0.947716 14.5 1.5 14.5H13.5C14.0523 14.5 14.5 14.0523 14.5 13.5V1.5C14.5 0.947715 14.0523 0.5 13.5 0.5Z" stroke="black"/> `;
	let svgsolid = `<path d="M1.5 0C0.671573 0 0 0.671574 0 1.5V13.5C0 14.3284 0.671573 15 1.5 15H13.5C14.3284 15 15 14.3284 15 13.5V1.5C15 0.671573 14.3284 0 13.5 0H1.5Z" fill="black"/> `;
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
	export let ariaLabel = 'square';
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
