<script lang="ts">
	export let size: string = '15';
	export let color: string = 'black';
	export let variation: 'solid' | 'outline' = 'outline';
	let svgpath: string;
	let svgoutline = `<path d="M7.5 1.5L7.85355 1.14645L7.5 0.792893L7.14645 1.14645L7.5 1.5ZM7.14645 1.85355L11.1464 5.85355L11.8536 5.14645L7.85355 1.14645L7.14645 1.85355ZM7.14645 1.14645L3.14645 5.14645L3.85355 5.85355L7.85355 1.85355L7.14645 1.14645ZM7 1.5V14H8V1.5H7Z" fill="${color}"/> `;
	let svgsolid = `<path fill-rule="evenodd" clip-rule="evenodd" d="M7.50001 0.792908L11.8536 5.14646L11.1465 5.85357L8.00001 2.70712V14H7.00001V2.70712L3.85356 5.85357L3.14645 5.14646L7.50001 0.792908Z" fill="${color}"/> `;
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
	export let ariaLabel = 'arrow up';
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
