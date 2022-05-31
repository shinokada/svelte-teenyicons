<script lang="ts">
	export let size = '15';
	export let ariaLabel = '360';
	export let variation: 'solid' | 'outline' = 'outline';
	let svgpath: string;
	let svgoutline = `<path d="M6.5 2.4987L6.14647 2.14512L5.79284 2.4987L6.14647 2.85228L6.5 2.4987ZM7.5 1.99878H7V2.99878H7.5V1.99878ZM2 8.49487V7.99487H1V8.49487H2ZM8.14547 0.14642L6.14647 2.14512L6.85353 2.85228L8.85253 0.85358L8.14547 0.14642ZM6.14647 2.85228L8.14547 4.85097L8.85253 4.14381L6.85353 2.14512L6.14647 2.85228ZM7.5 2.99878C10.5372 2.99878 13 5.46048 13 8.49487H14C14 4.90758 11.0888 1.99878 7.5 1.99878V2.99878ZM13 8.49487C13 11.5293 10.5372 13.991 7.5 13.991V14.991C11.0888 14.991 14 12.0822 14 8.49487H13ZM7.5 13.991C4.46283 13.991 2 11.5293 2 8.49487H1C1 12.0822 3.91117 14.991 7.5 14.991V13.991Z" fill="black"/> `;
	let svgsolid = `<path fill-rule="evenodd" clip-rule="evenodd" d="M8.14547 0.146423L8.85253 0.853584L7.70401 2.00192C11.1985 2.10967 14 4.97581 14 8.49487C14 12.0822 11.0888 14.991 7.5 14.991C3.91117 14.991 1 12.0822 1 8.49487V7.99487H2V8.49487C2 11.5293 4.46283 13.991 7.5 13.991C10.5372 13.991 13 11.5293 13 8.49487C13 5.53117 10.6506 3.11379 7.7113 3.00277L8.85253 4.14382L8.14547 4.85098L5.79284 2.4987L8.14547 0.146423Z" fill="black"/> `;
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
