<script lang="ts">
	export let size = '15';
	export let variation: 'solid' | 'outline' = 'outline';
	let svgpath: string;
	let svgoutline = `<path d="M0.5 0.5L6.5 14.5L8.5 8.5L14.5 6.5L0.5 0.5Z" stroke="black" stroke-linejoin="round"/> `;
	let svgsolid = `<path d="M0.696974 0.0404421C0.509053 -0.0400956 0.291031 0.00189163 0.146461 0.146461C0.00189163 0.291031 -0.0400956 0.509053 0.0404421 0.696974L6.04044 14.697C6.12222 14.8878 6.31338 15.0082 6.52079 14.9996C6.7282 14.991 6.90871 14.8551 6.97436 14.6581L8.8953 8.8953L14.6581 6.97436C14.8551 6.90871 14.991 6.7282 14.9996 6.52079C15.0082 6.31338 14.8878 6.12222 14.697 6.04044L0.696974 0.0404421Z" fill="black"/> `;
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
	export let ariaLabel = 'direction';
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
