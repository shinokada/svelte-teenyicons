<script>
  import { AdjustVertical, Youtube, Wordpress } from '$lib';
  const random_hex_color_code = () => {
    let n = (Math.random() * 0xfffff * 1000000).toString(16);
    return '#' + n.slice(0, 6);
  };
</script>

<AdjustVertical size="40" color={random_hex_color_code()} />
<AdjustVertical size="40" color={random_hex_color_code()} variation="solid" />
<AdjustVertical size="40" />

<Youtube size="40" color={random_hex_color_code()} />
<Youtube size="40" color={random_hex_color_code()} variation="solid" />
<Youtube size="40" />

<Wordpress size="40" color={random_hex_color_code()} />
<Wordpress size="40" color={random_hex_color_code()} variation="solid" />
<Wordpress size="40" />
