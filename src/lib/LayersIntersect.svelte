<script lang="ts">
	export let size = '15';
	export let variation: 'solid' | 'outline' = 'outline';
	let svgpath: string;
	let svgoutline = `<path d="M4.5 3V1.5C4.5 0.947715 4.94772 0.5 5.5 0.5H7M12 0.5H13.5C14.0523 0.5 14.5 0.947715 14.5 1.5V3M8 0.5H11M12 10.5H13.5C14.0523 10.5 14.5 10.0523 14.5 9.5V8M14.5 4V7M3 4.5H1.5C0.947715 4.5 0.5 4.94772 0.5 5.5V7M0.5 12V13.5C0.5 14.0523 0.947715 14.5 1.5 14.5H3M0.5 8V11M8 14.5H9.5C10.0523 14.5 10.5 14.0523 10.5 13.5V12M4 14.5H7M4.5 4.5V10.5H10.5V4.5H4.5Z" stroke="black"/> `;
	let svgsolid = `<path fill-rule="evenodd" clip-rule="evenodd" d="M4 1.5V4H1.5C0.671573 4 0 4.67157 0 5.5V13.5C0 14.3284 0.671573 15 1.5 15H9.5C10.3284 15 11 14.3284 11 13.5V11H13.5C14.3284 11 15 10.3284 15 9.5V1.5C15 0.671573 14.3284 0 13.5 0H5.5C4.67157 0 4 0.671573 4 1.5ZM5.5 1C5.22386 1 5 1.22386 5 1.5V4H9.5C10.3284 4 11 4.67157 11 5.5V10H13.5C13.7761 10 14 9.77614 14 9.5V1.5C14 1.22386 13.7761 1 13.5 1H5.5ZM5.5 11C4.67157 11 4 10.3284 4 9.5V5H1.5C1.22386 5 1 5.22386 1 5.5V13.5C1 13.7761 1.22386 14 1.5 14H9.5C9.77614 14 10 13.7761 10 13.5V11H5.5Z" fill="black"/> `;
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
	export let ariaLabel = 'layers intersect';
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
