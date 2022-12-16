<script lang="ts">
	export let size: string = '15';
	export let color: string = 'black';
	export let variation: 'solid' | 'outline' = 'outline';
	let svgpath: string;
	let svgoutline = `<path d="M15 0.5H0M11.5 3.5H8.5V10.5H11.5V3.5ZM6.5 3.5H3.5V14.5H6.5V3.5Z" stroke="${color}"/> `;
	let svgsolid = `<path d="M15 0H0V1H15V0Z" fill="${color}"/> <path d="M7 3H3V15H7V3Z" fill="${color}"/> <path d="M12 3H8V11H12V3Z" fill="${color}"/> `;
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
	export let ariaLabel = 'align top';
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
