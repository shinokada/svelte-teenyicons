<script lang="ts">
	export let size = '15';
	export let variation: 'solid' | 'outline' = 'outline';
	let svgpath: string;
	let svgoutline = `<path d="M14 8L7.5 1L1 8M14 13.5L7.5 6.5L1 13.5" stroke="black" stroke-linecap="square"/> `;
	let svgsolid = `<path fill-rule="evenodd" clip-rule="evenodd" d="M7.5 0.265198L14.7066 8.02618L13.9738 8.70663L7.5 1.73481L1.02617 8.70663L0.293381 8.02618L7.5 0.265198ZM7.5 5.7652L14.7066 13.5262L13.9738 14.2066L7.5 7.23481L1.02617 14.2066L0.293381 13.5262L7.5 5.7652Z" fill="black"/> `;
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
	export let ariaLabel = 'double caret up';
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
