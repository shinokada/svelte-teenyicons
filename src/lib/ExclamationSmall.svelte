<script lang="ts">
	export let size = '15';
	export let variation: 'solid' | 'outline' = 'outline';
	let svgpath: string;
	let svgoutline = `<path d="M8 10.5V10H7V10.5H8ZM7 10.51V11.01H8V10.51H7ZM7 4V8H8V4H7ZM7 10.5V10.51H8V10.5H7Z" fill="black"/> `;
	let svgsolid = `<path fill-rule="evenodd" clip-rule="evenodd" d="M7 8V4H8V8H7ZM8 10V11.01H7V10H8Z" fill="black"/> `;
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
	export let ariaLabel = 'exclamation small';
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
