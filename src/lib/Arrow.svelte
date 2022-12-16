<script lang="ts">
	export let size: string = '15';
	export let color: string = 'black';
	export let variation: 'solid' | 'outline' = 'outline';
	let svgpath: string;
	let svgoutline = `<path d="M0.5 0.5V0C0.223858 0 0 0.223858 0 0.5L0.5 0.5ZM0.5 4.5H0C0 4.70223 0.121821 4.88455 0.308658 4.96194C0.495495 5.03933 0.710554 4.99655 0.853553 4.85355L0.5 4.5ZM4.5 0.5L4.85355 0.853553C4.99655 0.710554 5.03933 0.495495 4.96194 0.308658C4.88455 0.121821 4.70223 0 4.5 0V0.5ZM2.14645 2.85355L14.1464 14.8536L14.8536 14.1464L2.85355 2.14645L2.14645 2.85355ZM0 0.5V4.5H1V0.5H0ZM0.853553 4.85355L4.85355 0.853553L4.14645 0.146447L0.146447 4.14645L0.853553 4.85355ZM4.5 0H0.5V1H4.5V0Z" fill="${color}"/> `;
	let svgsolid = `<path d="M4.5 0H0.5C0.223858 0 0 0.223858 0 0.5V4.5C0 4.70223 0.121821 4.88455 0.308658 4.96194C0.495495 5.03933 0.710554 4.99655 0.853553 4.85355L2.5 3.20711L14.1464 14.8536L14.8536 14.1464L3.20711 2.5L4.85355 0.853553C4.99655 0.710554 5.03933 0.495495 4.96194 0.308658C4.88455 0.121821 4.70223 0 4.5 0Z" fill="${color}"/> `;
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
	export let ariaLabel = 'arrow';
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
