<script lang="ts">
	export let size = '15';
	export let ariaLabel = '360';
	export let variation: 'solid' | 'outline' = 'outline';
	let svgpath: string;
	let svgoutline = `<path d="M2.5 1.5C2.5 2.05228 2.05228 2.5 1.5 2.5C0.947715 2.5 0.5 2.05228 0.5 1.5C0.5 0.947715 0.947715 0.5 1.5 0.5C2.05228 0.5 2.5 0.947715 2.5 1.5ZM2.5 1.5H7.5V13.5H12.5M12.5 13.5C12.5 14.0523 12.9477 14.5 13.5 14.5C14.0523 14.5 14.5 14.0523 14.5 13.5C14.5 12.9477 14.0523 12.5 13.5 12.5C12.9477 12.5 12.5 12.9477 12.5 13.5Z" stroke="black"/> `;
	let svgsolid = `<path d="M1.5 0C0.671573 0 0 0.671573 0 1.5C0 2.32843 0.671573 3 1.5 3C2.15311 3 2.70873 2.5826 2.91465 2H7V14H12.0854C12.2913 14.5826 12.8469 15 13.5 15C14.3284 15 15 14.3284 15 13.5C15 12.6716 14.3284 12 13.5 12C12.8469 12 12.2913 12.4174 12.0854 13H8V1H2.91465C2.70873 0.417404 2.15311 0 1.5 0Z" fill="black"/> `;
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
