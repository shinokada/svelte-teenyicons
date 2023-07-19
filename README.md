# Svelte Teenyicons

<div class="flex gap-2 my-8">
<a href="https://github.com/sponsors/shinokada" target="_blank"><img src="https://img.shields.io/static/v1?label=Sponsor&message=%E2%9D%A4&logo=GitHub&color=%23fe8e86" alt="sponsor" height="25" style="height: 25px !important;"></a>
<a href="https://www.npmjs.com/package/svelte-teenyicons" rel="nofollow" target="_blank"><img src="https://img.shields.io/npm/v/svelte-teenyicons" alt="npm" height="25" style="height: 25px !important;"></a>
<a href="https://twitter.com/shinokada" rel="nofollow" target="_blank"><img src="https://img.shields.io/badge/created%20by-@shinokada-4BBAAB.svg" alt="Created by Shin Okada" height="25" style="height: 25px !important;"></a>
<a href="https://opensource.org/licenses/MIT" rel="nofollow" target="_blank"><img src="https://img.shields.io/github/license/shinokada/svelte-teenyicons" alt="License" height="25" style="height: 25px !important;"></a>
<a href="https://www.npmjs.com/package/svelte-teenyicons" rel="nofollow" target="_blank"><img src="https://img.shields.io/npm/dw/svelte-teenyicons.svg" alt="npm" height="25" style="height: 25px !important;"></a>
</div>

600+ SVG TeenyIcons for Svelte.

Thank you for considering my open-source package. If you use it in a commercial project, please support me by sponsoring me on [GitHub sponsor](https://github.com/sponsors/shinokada). Your support helps me maintain and improve this package for the benefit of the community.

## Repo

[GitHub Repo](https://github.com/shinokada/svelte-teenyicons)

## Original source

[teenyicons/teenyicons](https://github.com/teenyicons/teenyicons)

## License

[Svelte-Teenyicons License](https://github.com/shinokada/svelte-teenyicons/LICENSE)

[teenyicons/teenyicons License](https://github.com/teenyicons/teenyicons/blob/master/LICENSE)

## Installation

```sh
pnpm i svelte-teenyicons
```

## Usage

```js
<script>
  import { Alarm } from "svelte-teenyicons";
</script>

<Alarm />
```

## Faster compiling

If you need only a few icons from this library in your Svelte app, import them directly. This can optimize compilation speed and improve performance by reducing the amount of code processed during compilation.

```html
<script>
  import Alarm from 'svelte-teenyicons/Alarm.svelte';
</script>

<Alarm />
```

If you are a TypeScript user, install **typescript version 5.0.0 or above**.

```sh
pnpm i -D typescript@beta
```

To avoid any complaints from the editor, add `node16` or `nodenext` to `moduleResolution` in your tsconfig.json file.

```json
{
  //...
  "compilerOptions": {
    // ...
    "moduleResolution": "nodenext"
  }
}
```

## Props

- size: string = '15';
- role: string = 'img';
- color: string = 'black';
- variation: 'solid' | 'outline' = 'outline';
- ariaLabel = 'icon file name';

## IDE support

If you are using an LSP-compatible editor, such as VSCode, Atom, Sublime Text, or Neovim, hovering over a component name will display a documentation link, features, props, events, and an example.

## Variation

The default variation value is outline. Use the `variation` prop to change it to solid.

```html
<AbTesting variation="solid" /> <AbTesting />
```

## Size

Use the `size` prop to change the size of icons.

```html
<AbTesting size="30" />
<AbTesting size="40" />
<AbTesting size="50" />
```

If you are using Tailwind CSS, you can add a custom size using Tailwind CSS by including the desired classes in the `class` prop. For example:

```html
<AbTesting class="shrink-0 h-20 w-20" />
```

## CSS HEX Colors

Use the `color` prop to change colors with HEX color code.

```html
<AbTesting color="#c61515" />
<AbTesting color="#3759e5" />
<AbTesting color="#3fe537" />
```

## CSS framework support

You can apply CSS framework color and other attributes directly to the icon component or its parent tag using the `class` prop.

For example, Tailwind CSS:

```html
<AbTesting class="mr-4" />
```

Bootstrap example:

```html
<AbTesting class="position-absolute top-0 px-1" />
```

## Dark mode

If you are using the dark mode on your website with Tailwind CSS, add your dark mode class to the `class` prop.

Let's use `dark` for the dark mode class as an example.

```html
<AbTesting class="text-blue-700 dark:text-red-500" />
```

## aria-label

All icons have aria-label. For example `AbTesting` has `aria-label="ab testing"`.
Use `ariaLabel` prop to modify the `aria-label` value.

```html
<AbTesting ariaLabel="AB testing icon" class="text-red-500" />
```

## Unfocusable icon

If you want to make an icon unfocusable, add `tabindex="-1"`.

```html
<AbTesting tabindex="-1" />
```

## Events

All icons have the following events:

```
on:click
on:mouseenter
on:mouseleave
on:mouseover
on:mouseout
on:blur
on:focus
```

## Passing down other attributes

You can pass other attibutes as well.

```html
<AbTesting tabindex="0"></AbTesting>
```

## Using svelte:component

```html
<script>
  import { AbTesting } from 'svelte-teenyicons';
</script>

<svelte:component this="{AbTesting}" />
```

## Using onMount

```html
<script>
  import { AbTesting } from 'svelte-teenyicons';
  import { onMount } from 'svelte';
  const props = {
    size: '50',
    color: '#ff0000'
  };
  onMount(() => {
    const icon = new AbTesting({ target: document.body, props });
  });
</script>
```

## Import all

Use `import * as Icon from 'svelte-teenyicons`.

```html
<script>
  import * as Icon from 'svelte-teenyicons';
</script>

<Icon.AbTesting size="30" class="mx-2" />
<Icon.Alarm size="40" class="mx-2" />
<Icon.MessageX size="50" class="mx-2" />
<Icon.Minimize size="60" class="mx-2" />
<Icon.Moon size="100" class="mx-2" tabindex="0" />
```

## Other icons

[Svelte-Icon-Sets](https://svelte-svg-icons.vercel.app/)
