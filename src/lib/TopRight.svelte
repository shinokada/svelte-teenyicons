<script lang="ts">
	export let size = '15';
	export let ariaLabel = '360';
	export let variation: 'solid' | 'outline' = 'outline';
	let svgpath: string;
	let svgoutline = `<path d="M13.5 1.5H14C14 1.22386 13.7761 1 13.5 1V1.5ZM13.5 1H8V2H13.5V1ZM13 1.5V7H14V1.5H13ZM13.1464 1.14645L1.14645 13.1464L1.85355 13.8536L13.8535 1.85355L13.1464 1.14645Z" fill="black"/> `;
	let svgsolid = `<path fill-rule="evenodd" clip-rule="evenodd" d="M8 1H14V7H13V2.70711L1.85355 13.8536L1.14645 13.1464L12.2929 2H8V1Z" fill="black"/> `;
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
