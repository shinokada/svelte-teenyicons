<script lang="ts">
	export let size = '15';
	export let variation: 'solid' | 'outline' = 'outline';
	let svgpath: string;
	let svgoutline = `<path d="M7.5 9V7.5H8C8.82843 7.5 9.5 6.82843 9.5 6V5.9C9.5 5.1268 8.8732 4.5 8.1 4.5H7.5C6.67157 4.5 6 5.17157 6 6M7 10.5H8" stroke="black"/> `;
	let svgsolid = `<path fill-rule="evenodd" clip-rule="evenodd" d="M5.5 6C5.5 4.89543 6.39543 4 7.5 4H8.1C9.14934 4 10 4.85066 10 5.9V6C10 7.10457 9.10457 8 8 8V9H7V7H8C8.55228 7 9 6.55228 9 6V5.9C9 5.40294 8.59706 5 8.1 5H7.5C6.94772 5 6.5 5.44772 6.5 6H5.5ZM8 10V11H7V10H8Z" fill="black"/> `;
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
	export let ariaLabel = 'question small';
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
