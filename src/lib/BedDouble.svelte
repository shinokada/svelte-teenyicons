<script lang="ts">
	export let size: string = '15';
	export let color: string = 'black';
	export let variation: 'solid' | 'outline' = 'outline';
	let svgpath: string;
	let svgoutline = `<path d="M14.5 7V15M0.5 7V15M0 10.5H15M0 7.5H15M2 5.5H6M9 5.5H13M0.5 6V0.5H14.5V6" stroke="${color}"/> `;
	let svgsolid = `<path d="M0 0H15V6H14V1H1V6H0V0Z" fill="${color}"/> <path d="M6 6H2V5H6V6Z" fill="${color}"/> <path d="M0 15H1V11H14V15H15V7H0V15Z" fill="${color}"/> <path d="M9 6H13V5H9V6Z" fill="${color}"/> `;
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
	export let ariaLabel = 'bed double';
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
