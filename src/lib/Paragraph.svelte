<script lang="ts">
	export let size = '15';
	export let variation: 'solid' | 'outline' = 'outline';
	let svgpath: string;
	let svgoutline = `<path d="M13 1.5H6.5C4.29086 1.5 2.5 3.29086 2.5 5.5C2.5 7.70914 4.29086 9.5 6.5 9.5H7.5M10.5 14V1.5M7.5 14V1.5" stroke="black"/> `;
	let svgsolid = `<path fill-rule="evenodd" clip-rule="evenodd" d="M2 5.5C2 3.01472 4.01472 1 6.5 1H13V2H11V14H10V2H8V14H7V10H6.5C4.01472 10 2 7.98528 2 5.5ZM7 9V2H6.5C4.567 2 3 3.567 3 5.5C3 7.433 4.567 9 6.5 9H7Z" fill="black"/> `;
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
	export let ariaLabel = 'paragraph';
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
