<script lang="ts">
	export let size = '15';
	export let variation: 'solid' | 'outline' = 'outline';
	let svgpath: string;
	let svgoutline = `<path d="M4 1.5H13M2 13.5H11M8.5 1.5L6.5 13.5" stroke="black"/> `;
	let svgsolid = `<path fill-rule="evenodd" clip-rule="evenodd" d="M7.90977 2H4V1H13V2H8.92356L7.09023 13H11V14H2V13H6.07644L7.90977 2Z" fill="black"/> `;
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
	export let ariaLabel = 'italic';
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
