<h1 align="center">Svelte Teenyicons</h1>

<p align="center">
<a href="https://svelte-teenyicons.codewithshin.com/">Svelte-Teenyicons</a>
</p>

<p align="center">
<a href="https://github.com/sponsors/shinokada" target="_blank"><img src="https://img.shields.io/static/v1?label=Sponsor&message=%E2%9D%A4&logo=GitHub&color=%23fe8e86" height="25"></a>
<a href="https://developer.mozilla.org/en-US/docs/Web/Progressive_web_apps" target="_blank"><img src="https://img.shields.io/badge/PWA-enabled-brightgreen" alt="PWA Shield" height="25">
</a>
<a href="https://www.npmjs.com/package/svelte-teenyicons" rel="nofollow" target="_blank"><img src="https://img.shields.io/npm/v/svelte-teenyicons" alt="npm" height="25"></a>
<a href="https://twitter.com/shinokada" rel="nofollow" target="_blank"><img src="https://img.shields.io/badge/created%20by-@shinokada-4BBAAB.svg" alt="Created by Shin Okada" height="25"></a>
<a href="https://opensource.org/licenses/MIT" rel="nofollow" target="_blank"><img src="https://img.shields.io/github/license/shinokada/svelte-teenyicons" alt="License" height="25"></a>
<a href="https://www.npmjs.com/package/svelte-teenyicons" rel="nofollow" target="_blank"><img src="https://img.shields.io/npm/dw/svelte-teenyicons.svg" alt="npm" height="25"></a>
</p>

SVG TeenyIcons for Svelte. You can import outline and solid icons without name conflict. Svlete-Teenyicons support major CSS framework. You can add additional CSS using the `class` props.

Thank you for considering my open-source package. If you use it in a commercial project, please support me by sponsoring me on GitHub: https://github.com/sponsors/shinokada. Your support helps me maintain and improve this package for the benefit of the community.

<p align="center">
<img width="650" src="/static/images/teeny-outline-optimized-650-1050.png" />
</p>

## Installation

```sh
npm i svelte-teenyicons
```

## Icon names

[Icon names](/icon-list.md)

## Icon images

[Icon images](/icon-images.md)

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

As of March 2023, the `typescript@beta` version is now available:

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

| Name                         | Default     |
| ---------------------------- | ----------- |
| size                         | 15          |
| class                        |             |
| color                        | black       |
| ariaLabel                    | <file name> |
| variation (solid or outline) | outline     |

## Variation

The default variation value is outline. Use the `variation` prop to change it to solid.

```html
<AbTesting variation="solid" /> <AbTesting />
```

## Faster compiling

If you need only a few icons from this library in your Svelte app, import them directly. This can optimize compilation speed and improve performance by reducing the amount of code processed during compilation.

```html
<script>
  import AbTesting from 'svelte-teenyicons/AbTesting.svelte';
</script>

<AbTesting />
```

If you are a TypeScript user, install **typescript version 5.0.0 or above**.

As of March 2023, the `typescript@beta` version is now available:

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

## Size

Use the `size` prop to change the size of icons.

```html
<AbTesting size="30" />
<AbTesting size="40" />
<AbTesting size="50" />
```

## CSS HEX Colors

Use the `color` prop to change colors with HEX color code.

```html
<AbTesting color="#c61515" />
<AbTesting color="#3759e5" />
<AbTesting color="#3fe537" />
```

## CSS framework support

Use the `class` prop to change colors and add additional css.

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

- [Svelte-Icon-Sets](https://svelte-svg-icons.vercel.app/)

## PWA: Fast & Offline

This website can be downloaded and installed on your device for offline access as a Progressive Web App.

To install a PWA, look for the "Add to Home Screen" option in the browser's menu or settings. On most mobile devices, this option can be found by visiting the website, then selecting the "Options" or "Menu" button in the browser, and looking for the "Add to Home Screen" option. On some desktop browsers, right-click on the page and select "Install".
