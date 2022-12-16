<script lang="ts">
	export let size: string = '15';
	export let color: string = 'black';
	export let variation: 'solid' | 'outline' = 'outline';
	let svgpath: string;
	let svgoutline = `<path d="M7.5 13.5L11.5 9.5M7.5 13.5L3.5 9.5M7.5 13.5V1" stroke="${color}"/> `;
	let svgsolid = `<path fill-rule="evenodd" clip-rule="evenodd" d="M8.00001 1V12.2929L11.1465 9.14645L11.8536 9.85355L7.50001 14.2071L3.14645 9.85355L3.85356 9.14645L7.00001 12.2929V1H8.00001Z" fill="${color}"/> `;
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
	export let ariaLabel = 'arrow down';
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
