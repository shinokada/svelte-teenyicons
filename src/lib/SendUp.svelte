<script lang="ts">
	export let size: string = '15';
	export let color: string = 'black';
	export let variation: 'solid' | 'outline' = 'outline';
	let svgpath: string;
	let svgoutline = `<path d="M7.5 1.5L11.5 5.5M7.5 1.5L3.5 5.5M7.5 1.5V12M1 13.5H14" stroke="${color}"/> `;
	let svgsolid = `<path fill-rule="evenodd" clip-rule="evenodd" d="M7.5 0.792892L11.8536 5.14645L11.1464 5.85355L8 2.70711V12H7V2.70711L3.85355 5.85355L3.14645 5.14645L7.5 0.792892ZM14 13V14H1V13H14Z" fill="${color}"/> `;
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
	export let ariaLabel = 'send up';
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
