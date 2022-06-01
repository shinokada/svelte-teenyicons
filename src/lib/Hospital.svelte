<script lang="ts">
	export let size = '15';
	export let variation: 'solid' | 'outline' = 'outline';
	let svgpath: string;
	let svgoutline = `<path d="M7.5 0.5L7.72361 0.0527864C7.58284 -0.0175955 7.41716 -0.0175955 7.27639 0.0527864L7.5 0.5ZM1.5 3.5L1.27639 3.05279C1.107 3.13748 1 3.31061 1 3.5H1.5ZM13.5 3.5H14C14 3.31061 13.893 3.13748 13.7236 3.05279L13.5 3.5ZM5.5 10.5V10H5V10.5H5.5ZM9.5 10.5H10V10H9.5V10.5ZM0 15H15V14H0V15ZM7.27639 0.0527864L1.27639 3.05279L1.72361 3.94721L7.72361 0.947214L7.27639 0.0527864ZM13.7236 3.05279L7.72361 0.0527864L7.27639 0.947214L13.2764 3.94721L13.7236 3.05279ZM7 3V5.5H8V3H7ZM7 5.5V8H8V5.5H7ZM5 6H7.5V5H5V6ZM7.5 6H10V5H7.5V6ZM1 3.5V14.5H2V3.5H1ZM13 3.5V14.5H14V3.5H13ZM6 14.5V10.5H5V14.5H6ZM5.5 11H9.5V10H5.5V11ZM9 10.5V14.5H10V10.5H9Z" fill="black"/> `;
	let svgsolid = `<path fill-rule="evenodd" clip-rule="evenodd" d="M7.72361 0.0527864C7.58285 -0.0175955 7.41716 -0.0175955 7.2764 0.0527864L1.28617 3.0479C1.117 3.12806 1 3.30037 1 3.5V14H0V15H5V10H10V15H15V14H14V3.5C14 3.30044 13.8831 3.12818 13.714 3.04799L7.72361 0.0527864ZM7 5V3H8V5H10V6H8V8H7V6H5V5H7Z" fill="black"/> <path d="M9 15V11H6V15H9Z" fill="black"/> `;
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
	export let ariaLabel = 'hospital';
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
