<script lang="ts">
	export let size = '15';
	export let variation: 'solid' | 'outline' = 'outline';
	let svgpath: string;
	let svgoutline = `<path d="M6.14645 9.85355L6.5 10.2071L7.20711 9.5L6.85355 9.14645L6.14645 9.85355ZM4.5 7.5L4.14645 7.14645L3.79289 7.5L4.14645 7.85355L4.5 7.5ZM6.85355 5.85355L7.20711 5.5L6.5 4.79289L6.14645 5.14645L6.85355 5.85355ZM6.85355 9.14645L4.85355 7.14645L4.14645 7.85355L6.14645 9.85355L6.85355 9.14645ZM4.85355 7.85355L6.85355 5.85355L6.14645 5.14645L4.14645 7.14645L4.85355 7.85355ZM4.5 8H11V7H4.5V8Z" fill="black"/> `;
	let svgsolid = `<path fill-rule="evenodd" clip-rule="evenodd" d="M7.20711 5.50001L5.70711 7.00001H11V8.00001H5.70711L7.20711 9.50001L6.5 10.2071L3.79289 7.50001L6.5 4.79291L7.20711 5.50001Z" fill="black"/> `;
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
	export let ariaLabel = 'arrow left small';
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
