<script lang="ts">
	export let size = '15';
	export let variation: 'solid' | 'outline' = 'outline';
	let svgpath: string;
	let svgoutline = `<path d="M7.5 15V8.5M7.5 8.5C9.70914 8.5 11.5 6.70914 11.5 4.5C11.5 2.29086 9.70914 0.5 7.5 0.5C5.29086 0.5 3.5 2.29086 3.5 4.5C3.5 6.70914 5.29086 8.5 7.5 8.5Z" stroke="black"/> `;
	let svgsolid = `<path d="M7.5 0C5.01472 0 3 2.01472 3 4.5C3 6.81628 4.75002 8.72381 7 8.97254V15H8V8.97254C10.25 8.72381 12 6.81628 12 4.5C12 2.01472 9.98528 0 7.5 0Z" fill="black"/> `;
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
	export let ariaLabel = 'pin alt';
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
