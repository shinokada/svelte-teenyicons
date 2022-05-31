<script lang="ts">
	export let size = '15';
	export let ariaLabel = '360';
	export let variation: 'solid' | 'outline' = 'outline';
	let svgpath: string;
	let svgoutline = `<path d="M11 1.5H13.5V13.5C13.5 14.0523 13.0523 14.5 12.5 14.5H2.5C1.94772 14.5 1.5 14.0523 1.5 13.5V1.5H4M9.5 6.5L5.5 10.5M4.5 0.5H10.5V2.5C10.5 3.05228 10.0523 3.5 9.5 3.5H5.5C4.94772 3.5 4.5 3.05228 4.5 2.5V0.5ZM7.5 11.5C5.84315 11.5 4.5 10.1569 4.5 8.5C4.5 6.84315 5.84315 5.5 7.5 5.5C9.15685 5.5 10.5 6.84315 10.5 8.5C10.5 10.1569 9.15685 11.5 7.5 11.5Z" stroke="black"/> `;
	let svgsolid = `<path d="M7.5 6C6.11929 6 5 7.11929 5 8.5C5 9.00954 5.15244 9.48349 5.4142 9.8787L8.8787 6.4142C8.48349 6.15244 8.00954 6 7.5 6Z" fill="black"/> <path d="M7.5 11C6.99046 11 6.51653 10.8476 6.12131 10.5858L9.58581 7.12131C9.84756 7.51653 10 7.99046 10 8.5C10 9.88071 8.88071 11 7.5 11Z" fill="black"/> <path fill-rule="evenodd" clip-rule="evenodd" d="M4 0H11V1H14V13.5C14 14.3284 13.3284 15 12.5 15H2.5C1.67157 15 1 14.3284 1 13.5V1H4V0ZM5 1H10V2.5C10 2.77614 9.77614 3 9.5 3H5.5C5.22386 3 5 2.77614 5 2.5V1ZM4 8.5C4 6.567 5.567 5 7.5 5C9.433 5 11 6.567 11 8.5C11 10.433 9.433 12 7.5 12C5.567 12 4 10.433 4 8.5Z" fill="black"/> `;
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
