<script lang="ts">
	export let size = '15';
	export let variation: 'solid' | 'outline' = 'outline';
	let svgpath: string;
	let svgoutline = `<path d="M0 5.5H6M0 1.5H6M0 9.5H15M0 13.5H15M9.5 0.5H13.5C14.0523 0.5 14.5 0.947715 14.5 1.5V5.5C14.5 6.05228 14.0523 6.5 13.5 6.5H9.5C8.94772 6.5 8.5 6.05228 8.5 5.5V1.5C8.5 0.947715 8.94772 0.5 9.5 0.5Z" stroke="black"/> `;
	let svgsolid = `<path d="M9.5 0C8.67157 0 8 0.671573 8 1.5V5.5C8 6.32843 8.67157 7 9.5 7H13.5C14.3284 7 15 6.32843 15 5.5V1.5C15 0.671573 14.3284 0 13.5 0H9.5Z" fill="black"/> <path d="M0 2H6V1H0V2Z" fill="black"/> <path d="M0 6H6V5H0V6Z" fill="black"/> <path d="M0 10H15V9H0V10Z" fill="black"/> <path d="M0 14H15V13H0V14Z" fill="black"/> `;
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
	export let ariaLabel = 'float right';
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
