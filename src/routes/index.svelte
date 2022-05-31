<script>
	import Icon from './Icon.svelte';
	const random_hex_color_code = () => {
		let n = (Math.random() * 0xfffff * 1000000).toString(16);
		return '#' + n.slice(0, 6);
	};
</script>

<Icon variation="solid" size="100" />
<Icon variation="outline" size="100" />

<Icon variation="solid" size="100" color={random_hex_color_code()} />

<Icon variation="outline" size="100" color={random_hex_color_code()} />
