<script lang="ts">
	export let size = '15';
	export let ariaLabel = '360';
	export let variation: 'solid' | 'outline' = 'outline';
	let svgpath: string;
	let svgoutline = `<path d="M6.85355 5.85355L7.20711 5.5L6.5 4.79289L6.14645 5.14645L6.85355 5.85355ZM4.5 7.5L4.14645 7.14645L3.79289 7.5L4.14645 7.85355L4.5 7.5ZM6.14645 9.85355L6.5 10.2071L7.20711 9.5L6.85355 9.14645L6.14645 9.85355ZM7.5 0.5V0V0.5ZM14.5 7.5H15H14.5ZM0.5 7.5H1H0.5ZM7.5 14.5V14V14.5ZM6.14645 5.14645L4.14645 7.14645L4.85355 7.85355L6.85355 5.85355L6.14645 5.14645ZM4.14645 7.85355L6.14645 9.85355L6.85355 9.14645L4.85355 7.14645L4.14645 7.85355ZM4.5 8L11 8V7L4.5 7V8ZM7.5 1C11.0899 1 14 3.91015 14 7.5H15C15 3.35786 11.6421 3.57628e-07 7.5 0V1ZM1 7.5C1 3.91015 3.91015 1 7.5 1V0C3.35786 -3.57628e-07 3.57628e-07 3.35786 0 7.5H1ZM7.5 14C3.91015 14 1 11.0899 1 7.5H0C-3.57628e-07 11.6421 3.35786 15 7.5 15V14ZM7.5 15C11.6421 15 15 11.6421 15 7.5H14C14 11.0899 11.0899 14 7.5 14V15Z" fill="black"/> `;
	let svgsolid = `<path fill-rule="evenodd" clip-rule="evenodd" d="M15.0001 7.5C15.0001 11.6421 11.6422 15 7.50009 15C3.35796 15 9.11906e-05 11.6421 9.15527e-05 7.5C9.19149e-05 3.35786 3.35796 -3.62117e-07 7.50009 0C11.6422 3.62117e-07 15.0001 3.35786 15.0001 7.5ZM6.50002 10.2072L3.79291 7.50005L6.50002 4.79294L7.20712 5.50005L5.70717 7L11.0001 7L11.0001 8L5.70708 8L7.20712 9.50005L6.50002 10.2072Z" fill="black"/> `;
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
