<script lang="ts">
	export let size: string = '15';
	export let color: string = 'black';
	export let variation: 'solid' | 'outline' = 'outline';
	let svgpath: string;
	let svgoutline = `<path d="M3.5 10C3.5 11.933 5.067 13.5 7 13.5H8.48686C10.151 13.5 11.5 12.151 11.5 10.4869C11.5 9.28151 10.6079 7.97481 9.5 7.5M6.07999 6.17714C5.12147 5.76635 4.5 4.82386 4.5 3.78103C4.5 2.52125 5.52125 1.5 6.78103 1.5H8C9.38071 1.5 10.5 2.61929 10.5 4M2 7.5H13" stroke="${color}"/> `;
	let svgsolid = `<path fill-rule="evenodd" clip-rule="evenodd" d="M4 3.78103C4 2.24511 5.24511 1 6.78103 1H8C9.65685 1 11 2.34315 11 4H10C10 2.89543 9.10457 2 8 2H6.78103C5.79739 2 5 2.79739 5 3.78103C5 4.62384 5.50228 5.38556 6.27694 5.71756L5.88303 6.63671C4.74067 6.14713 4 5.02387 4 3.78103ZM9.39164 8H2V7H13V8H10.9901C11.1132 8.13953 11.227 8.28706 11.3302 8.44014C11.7355 9.04196 12 9.76555 12 10.4869C12 12.4271 10.4271 14 8.48686 14H7C4.79086 14 3 12.2091 3 10H4C4 11.6569 5.34315 13 7 13H8.48686C9.87483 13 11 11.8748 11 10.4869C11 10.0028 10.8184 9.47038 10.5008 8.99881C10.2041 8.55844 9.80981 8.20245 9.39164 8Z" fill="${color}"/> `;
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
	export let ariaLabel = 'strikethrough';
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
