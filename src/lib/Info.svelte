<script lang="ts">
	export let size = '15';
	export let variation: 'solid' | 'outline' = 'outline';
	let svgpath: string;
	let svgoutline = `<path d="M7 1.49999V1.99999H8V1.49999H7ZM8 1.48999V0.98999H7V1.48999H8ZM8 13.5L8 3.99999H7L7 13.5H8ZM8 1.49999V1.48999H7V1.49999H8ZM4 4.99999H7.5V3.99999H4V4.99999ZM2 14H13V13H2V14Z" fill="black"/> `;
	let svgsolid = `<path fill-rule="evenodd" clip-rule="evenodd" d="M8 0.98999V1.99999H7V0.98999H8ZM7 13H2V14H13V13H8L8 3.99999L4 3.99999V4.99999H7L7 13Z" fill="black"/> `;
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
	export let ariaLabel = 'info';
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
