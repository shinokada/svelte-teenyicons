<script lang="ts">
	export let size = '15';
	export let variation: 'solid' | 'outline' = 'outline';
	let svgpath: string;
	let svgoutline = `<path d="M0.5 3.49805L7.5 0.5L14.5 3.49805M0.5 3.49805L7.5 6.49609M0.5 3.49805V3.5M14.5 3.49805L7.5 6.49609M14.5 3.49805V11.5L7.5 14.5M14.5 3.49805L7.5 6.5V14.5M7.5 6.49609V14.5M7.5 6.49609L0.5 3.5M7.5 14.5L0.5 11.5V3.5" stroke="black" stroke-linejoin="round"/> `;
	let svgsolid = `<path d="M7.30298 0.0404275C7.42875 -0.0134758 7.57112 -0.0134758 7.6969 0.0404275L14.5 2.95605L7.50002 5.95604L0.499949 2.95601L7.30298 0.0404275Z" fill="black"/> <path d="M-6.10352e-05 3.82969V11.5C-6.10352e-05 11.7 0.119137 11.8808 0.302979 11.9596L6.99994 14.8297V6.82969L-6.10352e-05 3.82969Z" fill="black"/> <path d="M7.99994 6.82976L14.9999 3.82976V11.5C14.9999 11.7 14.8807 11.8808 14.6969 11.9596L7.99994 14.8297V6.82976Z" fill="black"/> `;
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
	export let ariaLabel = 'box';
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
