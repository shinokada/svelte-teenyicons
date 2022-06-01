<script lang="ts">
	export let size = '15';
	export let variation: 'solid' | 'outline' = 'outline';
	let svgpath: string;
	let svgoutline = `<path d="M1 1.5H2M7 1.5H8M10 1.5H11M13 1.5H14M13 4.5H14M7 4.5H8M13 10.5H14M7 10.5H8M13 13.5H14M10 13.5H11M7 13.5H8M4 13.5H5M1 13.5H2M1 10.5H2M1 4.5H2M4 1.5H5M1 7.5H14" stroke="black"/> `;
	let svgsolid = `<path fill-rule="evenodd" clip-rule="evenodd" d="M2 2H1V1H2V2ZM5 2H4V1H5V2ZM8 2H7V1H8V2ZM11 2H10V1H11V2ZM14 2H13V1H14V2ZM2 5H1V4H2V5ZM8 5H7V4H8V5ZM14 5H13V4H14V5ZM14 8H1V7H14V8ZM2 11H1V10H2V11ZM8 11H7V10H8V11ZM14 11H13V10H14V11ZM2 14H1V13H2V14ZM5 14H4V13H5V14ZM8 14H7V13H8V14ZM11 14H10V13H11V14ZM14 14H13V13H14V14Z" fill="black"/> `;
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
	export let ariaLabel = 'border horizontal';
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
