<script lang="ts">
	export let size: string = '15';
	export let color: string = 'black';
	export let variation: 'solid' | 'outline' = 'outline';
	let svgpath: string;
	let svgoutline = `<path d="M6.5 9.5L4.5 7.5L6.5 5.5M9.5 9.5L7.5 7.5L9.5 5.5" stroke="${color}" stroke-linecap="square"/> `;
	let svgsolid = `<path fill-rule="evenodd" clip-rule="evenodd" d="M7.20712 5.50001L5.20712 7.50001L7.20712 9.50001L6.50001 10.2071L3.79291 7.50001L6.50001 4.79291L7.20712 5.50001ZM10.2071 5.50001L8.20712 7.50001L10.2071 9.50001L9.50001 10.2071L6.79291 7.50001L9.50001 4.79291L10.2071 5.50001Z" fill="${color}"/> `;
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
	export let ariaLabel = 'double caret left small';
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
