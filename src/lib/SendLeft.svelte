<script lang="ts">
	export let size = '15';
	export let variation: 'solid' | 'outline' = 'outline';
	let svgpath: string;
	let svgoutline = `<path d="M1.5 7.5L5.5 3.5M1.5 7.5L5.5 11.5M1.5 7.5H12M13.5 14V1" stroke="black"/> `;
	let svgsolid = `<path fill-rule="evenodd" clip-rule="evenodd" d="M13 1H14V14H13V1ZM2.70711 8L5.85355 11.1464L5.14645 11.8536L0.792892 7.5L5.14645 3.14645L5.85355 3.85355L2.70711 7H12V8H2.70711Z" fill="black"/> `;
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
	export let ariaLabel = 'send left';
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
