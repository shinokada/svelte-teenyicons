<script lang="ts">
	export let size = '15';
	export let variation: 'solid' | 'outline' = 'outline';
	let svgpath: string;
	let svgoutline = `<path d="M8.5 8.5L10.5 10.5M7 9.5C5.61929 9.5 4.5 8.38071 4.5 7C4.5 5.61929 5.61929 4.5 7 4.5C8.38071 4.5 9.5 5.61929 9.5 7C9.5 8.38071 8.38071 9.5 7 9.5Z" stroke="black"/> `;
	let svgsolid = `<path d="M7 4C5.34315 4 4 5.34315 4 7C4 8.65685 5.34315 10 7 10C7.64792 10 8.24786 9.7946 8.73827 9.44537L10.1464 10.8536L10.8536 10.1464L9.44537 8.73827C9.7946 8.24786 10 7.64792 10 7C10 5.34315 8.65685 4 7 4Z" fill="black"/> `;
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
	export let ariaLabel = 'search small';
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
