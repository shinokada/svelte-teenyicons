<script lang="ts">
	export let size = '15';
	export let variation: 'solid' | 'outline' = 'outline';
	let svgpath: string;
	let svgoutline = `<path d="M4.9 8.7L4.6 8.3L3.8 8.9L4.1 9.3L4.9 8.7ZM10.9 9.3L11.2 8.9L10.4 8.3L10.1 8.7L10.9 9.3ZM7.5 14C3.91015 14 1 11.0899 1 7.5H0C0 11.6421 3.35786 15 7.5 15V14ZM14 7.5C14 11.0899 11.0899 14 7.5 14V15C11.6421 15 15 11.6421 15 7.5H14ZM7.5 1C11.0899 1 14 3.91015 14 7.5H15C15 3.35786 11.6421 0 7.5 0V1ZM7.5 0C3.35786 0 0 3.35786 0 7.5H1C1 3.91015 3.91015 1 7.5 1V0ZM4 6H5V5H4V6ZM10 6H11V5H10V6ZM10.1 8.7C8.8 10.4333 6.2 10.4333 4.9 8.7L4.1 9.3C5.8 11.5667 9.2 11.5667 10.9 9.3L10.1 8.7Z" fill="black"/> `;
	let svgsolid = `<path fill-rule="evenodd" clip-rule="evenodd" d="M0 7.5C0 3.35786 3.35786 0 7.5 0C11.6421 0 15 3.35786 15 7.5C15 11.6421 11.6421 15 7.5 15C3.35786 15 0 11.6421 0 7.5ZM4 6H5V5H4V6ZM10 6H11V5H10V6ZM4.9001 8.7C6.2001 10.4333 8.8001 10.4333 10.1001 8.7L10.9001 9.3C9.2001 11.5667 5.8001 11.5667 4.1001 9.3L4.9001 8.7Z" fill="black"/> `;
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
	export let ariaLabel = 'mood smile';
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
