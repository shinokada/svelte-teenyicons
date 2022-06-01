<script lang="ts">
	export let size = '15';
	export let variation: 'solid' | 'outline' = 'outline';
	let svgpath: string;
	let svgoutline = `<path d="M2 14.5H13M7.5 10.5V14.5M0 7.5H15M0.5 1.5L0.5 9.5C0.5 10.0523 0.947715 10.5 1.5 10.5L13.5 10.5C14.0523 10.5 14.5 10.0523 14.5 9.5V1.5C14.5 0.947716 14.0523 0.500001 13.5 0.500001L1.5 0.5C0.947715 0.5 0.5 0.947716 0.5 1.5Z" stroke="black"/> `;
	let svgsolid = `<path d="M13.5 0C14.3284 0 15 0.671573 15 1.5V7H0V1.5C0 0.671573 0.671573 0 1.5 0H13.5Z" fill="black"/> <path d="M0 8V9.5C0 10.3284 0.671573 11 1.5 11H7V14H2V15H13V14H8V11H13.5C14.3284 11 15 10.3284 15 9.5V8H0Z" fill="black"/> `;
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
	export let ariaLabel = 'imac';
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
