<script lang="ts">
	export let size = '15';
	export let variation: 'solid' | 'outline' = 'outline';
	let svgpath: string;
	let svgoutline = `<path d="M10.5 7.5L7.5 10.75M10.5 7.5L7.5 4.5M10.5 7.5L1 7.5M7 1.5L13.5 1.5V13.5H7" stroke="black"/> `;
	let svgsolid = `<path fill-rule="evenodd" clip-rule="evenodd" d="M7 1L14 1V14H7V13H13V2L7 2V1ZM7.85355 4.14645L11.1932 7.48614L7.8674 11.0891L7.13259 10.4109L9.358 8L0.999996 8V7L9.29289 7L7.14644 4.85355L7.85355 4.14645Z" fill="black"/> `;
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
	export let ariaLabel = 'signin';
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
