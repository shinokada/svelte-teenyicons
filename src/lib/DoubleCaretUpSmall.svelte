<script lang="ts">
	export let size = '15';
	export let variation: 'solid' | 'outline' = 'outline';
	let svgpath: string;
	let svgoutline = `<path d="M5.5 6.5L7.5 4.5L9.5 6.5M5.5 9.5L7.5 7.5L9.5 9.5" stroke="black" stroke-linecap="square"/> `;
	let svgsolid = `<path fill-rule="evenodd" clip-rule="evenodd" d="M7.5 3.79291L10.2071 6.50001L9.5 7.20712L7.5 5.20712L5.5 7.20712L4.79289 6.50001L7.5 3.79291ZM7.5 6.79291L10.2071 9.50001L9.5 10.2071L7.5 8.20712L5.5 10.2071L4.79289 9.50001L7.5 6.79291Z" fill="black"/> `;
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
	export let ariaLabel = 'double caret up small';
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
