<script lang="ts">
	export let size = '15';
	export let ariaLabel = '360';
	export let variation: 'solid' | 'outline' = 'outline';
	let svgpath: string;
	let svgoutline = `<path d="M0.5 14.5L8.5 6.5M2.5 12.5L4.5 14.5M4.5 10.5L6.5 12.5M11 7.5C9.067 7.5 7.5 5.933 7.5 4C7.5 2.067 9.067 0.5 11 0.5C12.933 0.5 14.5 2.067 14.5 4C14.5 5.933 12.933 7.5 11 7.5Z" stroke="black"/> `;
	let svgsolid = `<path fill-rule="evenodd" clip-rule="evenodd" d="M7 4C7 1.79086 8.79086 0 11 0C13.2091 0 15 1.79086 15 4C15 6.20914 13.2091 8 11 8C10.0756 8 9.22452 7.68646 8.54718 7.15993L5.20711 10.5L6.85355 12.1464L6.14645 12.8536L4.5 11.2071L3.20711 12.5L4.85355 14.1464L4.14645 14.8536L2.5 13.2071L0.853553 14.8536L0.146447 14.1464L7.84007 6.45282C7.31354 5.77548 7 4.92436 7 4ZM11 1C9.34315 1 8 2.34315 8 4C8 5.65685 9.34315 7 11 7C12.6569 7 14 5.65685 14 4C14 2.34315 12.6569 1 11 1Z" fill="black"/> `;
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
