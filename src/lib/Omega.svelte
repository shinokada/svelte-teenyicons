<script lang="ts">
	export let size: string = '15';
	export let color: string = 'black';
	export let variation: 'solid' | 'outline' = 'outline';
	let svgpath: string;
	let svgoutline = `<path d="M9.33338 11.6872C9.07302 11.7792 8.93656 12.0649 9.02858 12.3252C9.1206 12.5856 9.40627 12.722 9.66662 12.63L9.33338 11.6872ZM5.33338 12.63C5.59373 12.722 5.8794 12.5856 5.97142 12.3252C6.06344 12.0649 5.92698 11.7792 5.66662 11.6872L5.33338 12.63ZM5.5 14.5V15H6V14.5H5.5ZM9.5 14.5H9V15H9.5V14.5ZM7.5 1C10.5376 1 13 3.46243 13 6.5H14C14 2.91015 11.0899 0 7.5 0V1ZM7.5 0C3.91015 0 1 2.91015 1 6.5H2C2 3.46243 4.46243 1 7.5 1V0ZM13 6.5C13 8.89395 11.4702 10.9319 9.33338 11.6872L9.66662 12.63C12.1905 11.7379 14 9.33092 14 6.5H13ZM5.66662 11.6872C3.52976 10.9319 2 8.89395 2 6.5H1C1 9.33092 2.80947 11.7379 5.33338 12.63L5.66662 11.6872ZM0 15H5.5V14H0V15ZM6 14.5V12H5V14.5H6ZM15 14H9.5V15H15V14ZM10 14.5V12H9V14.5H10Z" fill="${color}"/> `;
	let svgsolid = `<path fill-rule="evenodd" clip-rule="evenodd" d="M1 6.5C1 2.91015 3.91015 0 7.5 0C11.0899 0 14 2.91015 14 6.5C14 9.20465 12.3484 11.5224 10 12.5017V14H15V15H9V12.1702C8.99982 12.1625 8.99982 12.1547 9 12.147V12H9.02579C9.07304 11.8591 9.18237 11.7405 9.33338 11.6872C11.4702 10.9319 13 8.89395 13 6.5C13 3.46243 10.5376 1 7.5 1C4.46243 1 2 3.46243 2 6.5C2 8.89395 3.52976 10.9319 5.66662 11.6872C5.81763 11.7405 5.92696 11.8591 5.97421 12H6V12.147C6.00018 12.1547 6.00018 12.1624 6 12.1702V15H0V14H5V12.5017C2.65164 11.5224 1 9.20465 1 6.5Z" fill="${color}"/> `;
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
	export let ariaLabel = 'omega';
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
