<script lang="ts">
	export let size = '15';
	export let ariaLabel = '360';
	export let variation: 'solid' | 'outline' = 'outline';
	let svgpath: string;
	let svgoutline = `<path d="M6.5 9.5V5.5L10 7.5L6.5 9.5Z" stroke="black" stroke-linejoin="round"/> `;
	let svgsolid = `<path d="M6.74807 5.06588C6.59332 4.97745 6.40319 4.97808 6.24904 5.06754C6.09488 5.15701 6 5.32176 6 5.5V9.5C6 9.67824 6.09488 9.84299 6.24904 9.93246C6.40319 10.0219 6.59332 10.0226 6.74807 9.93412L10.2481 7.93412C10.4039 7.8451 10.5 7.67943 10.5 7.5C10.5 7.32057 10.4039 7.1549 10.2481 7.06588L6.74807 5.06588Z" fill="black"/> `;
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
