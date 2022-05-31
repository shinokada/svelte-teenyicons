<script lang="ts">
	export let size = '15';
	export let ariaLabel = '360';
	export let variation: 'solid' | 'outline' = 'outline';
	let svgpath: string;
	let svgoutline = `<path d="M7.5 12V10.7361C7.5 9.36566 8.27427 8.11287 9.5 7.5C10.7257 6.88713 11.5 5.61338 11.5 4.24297C11.5 2.19498 9.83978 0.5 7.7918 0.5H7.58498C6.24999 0.5 4.96968 1.03032 4.02569 1.97431L3.5 2.5M7 14.5H8" stroke="black"/> `;
	let svgsolid = `<path fill-rule="evenodd" clip-rule="evenodd" d="M3.67215 1.62075C4.7099 0.583002 6.11739 0 7.58499 0H7.7918C10.122 0 12 1.92493 12 4.24297C12 5.7995 11.1216 7.2482 9.72361 7.94721C8.66727 8.47538 8.00001 9.55504 8.00001 10.7361V12H7.00001V10.7361C7.00001 9.17627 7.88128 7.75035 9.2764 7.05279C10.3298 6.52607 11 5.42726 11 4.24297C11 2.46504 9.5576 1 7.7918 1H7.58499C6.38261 1 5.22947 1.47765 4.37925 2.32786L3.85356 2.85355L3.14645 2.14645L3.67215 1.62075ZM8.00001 15H7.00001V14H8.00001V15Z" fill="black"/> `;
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
