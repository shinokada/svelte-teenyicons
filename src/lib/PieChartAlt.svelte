<script lang="ts">
	export let size = '15';
	export let variation: 'solid' | 'outline' = 'outline';
	let svgpath: string;
	let svgoutline = `<path d="M6.5 0.5V0C6.22386 0 6 0.223858 6 0.5L6.5 0.5ZM14.5 8.5V9C14.7761 9 15 8.77614 15 8.5H14.5ZM6.5 8.5H6V9H6.5V8.5ZM6.5 15C10.0899 15 13 12.0899 13 8.5H12C12 11.5376 9.53757 14 6.5 14V15ZM0 8.5C0 12.0899 2.91015 15 6.5 15V14C3.46243 14 1 11.5376 1 8.5H0ZM1 8.5C1 5.46243 3.46243 3 6.5 3V2C2.91015 2 0 4.91015 0 8.5H1ZM6.5 1C10.6421 1 14 4.35786 14 8.5H15C15 3.80558 11.1944 0 6.5 0V1ZM6 0.5V8.5H7V0.5H6ZM6.5 9H14.5V8H6.5V9Z" fill="black"/> `;
	let svgsolid = `<path d="M6.5 0H6V9H15V8.5C15 3.80558 11.1944 0 6.5 0Z" fill="black"/> <path d="M12.8261 10H5V2.17393C2.1333 2.8511 0 5.42642 0 8.5C0 12.0899 2.91015 15 6.5 15C9.57358 15 12.1489 12.8667 12.8261 10Z" fill="black"/> `;
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
	export let ariaLabel = 'pie chart alt';
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
