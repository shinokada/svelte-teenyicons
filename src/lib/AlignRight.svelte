<script lang="ts">
	export let size = '15';
	export let variation: 'solid' | 'outline' = 'outline';
	let svgpath: string;
	let svgoutline = `<path d="M14.5 0V15M11.5 3.5V6.5H4.5V3.5H11.5ZM11.5 8.5V11.5H0.5V8.5H11.5Z" stroke="black"/> `;
	let svgsolid = `<path d="M14 0V15H15V0H14Z" fill="black"/> <path d="M12 3H4V7H12V3Z" fill="black"/> <path d="M12 8H0V12H12V8Z" fill="black"/> `;
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
	export let ariaLabel = 'align right';
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
