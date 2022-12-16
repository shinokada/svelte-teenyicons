<script lang="ts">
	export let size: string = '15';
	export let color: string = 'black';
	export let variation: 'solid' | 'outline' = 'outline';
	let svgpath: string;
	let svgoutline = `<path d="M7.5 1V9.5M7.5 9.5V11.5C7.5 12.6046 6.60457 13.5 5.5 13.5C4.39543 13.5 3.5 12.6046 3.5 11.5C3.5 10.3954 4.39543 9.5 5.5 9.5M7.5 9.5H5.5M5.5 9.5C4.39543 9.5 3.5 8.60457 3.5 7.5C3.5 6.39543 4.39543 5.5 5.5 5.5M5.5 5.5H7.5M5.5 5.5H9.5M5.5 5.5C4.39543 5.5 3.5 4.60457 3.5 3.5C3.5 2.39543 4.39543 1.5 5.5 1.5H9.5C10.6046 1.5 11.5 2.39543 11.5 3.5C11.5 4.60457 10.6046 5.5 9.5 5.5M9.5 5.5C10.6046 5.5 11.5 6.39543 11.5 7.5C11.5 8.60457 10.6046 9.5 9.5 9.5C8.39543 9.5 7.5 8.60457 7.5 7.5C7.5 6.39543 8.39543 5.5 9.5 5.5Z" stroke="${color}"/> `;
	let svgsolid = `<path d="M3.99976 9.5C3.39267 9.04388 3 8.3178 3 7.5C3 6.6822 3.39267 5.95611 3.99976 5.5C3.39267 5.04388 3 4.3178 3 3.5C3 2.11929 4.11929 1 5.5 1H9.5C10.8807 1 12 2.11929 12 3.5C12 4.3178 11.6073 5.04388 11.0002 5.5C11.6073 5.95611 12 6.6822 12 7.5C12 8.88071 10.8807 10 9.5 10C8.9372 10 8.41783 9.81403 8 9.50018V11.5C8 12.8807 6.88071 14 5.5 14C4.11929 14 3 12.8807 3 11.5C3 10.6822 3.39267 9.95611 3.99976 9.5Z" fill="${color}"/> `;
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
	export let ariaLabel = 'figma';
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
