<script lang="ts">
	export let size = '15';
	export let variation: 'solid' | 'outline' = 'outline';
	let svgpath: string;
	let svgoutline = `<path d="M0.5 5.5H14.5M2 9.5H8M10 9.5H13M0.5 3.5L0.5 11.5C0.5 12.0523 0.947716 12.5 1.5 12.5L13.5 12.5C14.0523 12.5 14.5 12.0523 14.5 11.5V3.5C14.5 2.94772 14.0523 2.5 13.5 2.5L1.5 2.5C0.947716 2.5 0.5 2.94772 0.5 3.5Z" stroke="black"/> `;
	let svgsolid = `<path d="M13.5 2C14.3284 2 15 2.67157 15 3.5V5H0V3.5C0 2.67157 0.671573 2 1.5 2H13.5Z" fill="black"/> <path fill-rule="evenodd" clip-rule="evenodd" d="M0 6V11.5C0 12.3284 0.671573 13 1.5 13L13.5 13C14.3284 13 15 12.3284 15 11.5V6H0ZM2 10H8V9H2V10ZM13 10H10V9H13V10Z" fill="black"/> `;
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
	export let ariaLabel = 'credit card';
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
