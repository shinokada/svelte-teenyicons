<script lang="ts">
	export let size: string = '15';
	export let color: string = 'black';
	export let variation: 'solid' | 'outline' = 'outline';
	let svgpath: string;
	let svgoutline = `<path d="M10.5 7.5C10.5 9.15685 9.15685 10.5 7.5 10.5C5.84315 10.5 4.5 9.15685 4.5 7.5C4.5 5.84315 5.84315 4.5 7.5 4.5C9.15685 4.5 10.5 5.84315 10.5 7.5ZM10.5 7.5V8.5C10.5 9.60457 11.3954 10.5 12.5 10.5C13.2095 10.5 13.8328 10.1305 14.1878 9.57343C14.3855 9.26329 14.5 8.89502 14.5 8.5V7.5C14.5 3.63401 11.366 0.5 7.5 0.5C3.63401 0.5 0.5 3.63401 0.5 7.5C0.5 11.366 3.63401 14.5 7.5 14.5C8.98725 14.5 10.3662 14.0362 11.5 13.2453" stroke="${color}"/> `;
	let svgsolid = `<path fill-rule="evenodd" clip-rule="evenodd" d="M0 7.5C0 3.35786 3.35786 0 7.5 0C11.6421 0 15 3.35786 15 7.5V8.5C15 8.99302 14.8568 9.45412 14.6095 9.84215C14.1665 10.5372 13.3875 11 12.5 11C11.5285 11 10.6864 10.4458 10.2726 9.63634C9.63256 10.4658 8.62867 11 7.5 11C5.567 11 4 9.433 4 7.5C4 5.567 5.567 4 7.5 4C9.433 4 11 5.567 11 7.5V8.5C11 9.32843 11.6716 10 12.5 10C13.0316 10 13.4991 9.7238 13.7662 9.30471C13.9142 9.07247 14 8.79702 14 8.5V7.5C14 3.91015 11.0899 1 7.5 1C3.91015 1 1 3.91015 1 7.5C1 11.0899 3.91015 14 7.5 14C8.88168 14 10.1613 13.5695 11.214 12.8352L11.786 13.6554C10.571 14.5029 9.09282 15 7.5 15C3.35786 15 0 11.6421 0 7.5ZM10 7.5C10 6.11929 8.88071 5 7.5 5C6.11929 5 5 6.11929 5 7.5C5 8.88071 6.11929 10 7.5 10C8.88071 10 10 8.88071 10 7.5Z" fill="${color}"/> `;
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
	export let ariaLabel = 'at';
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
