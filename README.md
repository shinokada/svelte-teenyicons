# Svelte-Teenyicons

Monochrome SVG TeenyIcons for Svelte. You can import outline and solid icons without name conflict. Svlete-Teenyicons support major CSS framework. You can add additional CSS using the `class` props.

<p align="center">
<img width="450" src="https://raw.githubusercontent.com/shinokada/svelte-teenyicons/main/static/images/teeny1.webp" />
<img width="450" src="https://raw.githubusercontent.com/shinokada/svelte-teenyicons/main/static/images/teeny2.webp" />
<img width="450" src="https://raw.githubusercontent.com/shinokada/svelte-teenyicons/main/static/images/teeny3.webp" />
<img width="450" src="https://raw.githubusercontent.com/shinokada/svelte-teenyicons/main/static/images/teeny4.webp" />
</p>

## List of icons

[Icon names](https://github.com/shinokada/svelte-teenyicons/blob/main/icon-list.md)

## Installation

```sh
npm i svelte-teenyicons
```

## REPL

## Usage

```js
<script>import {(AbTesting, Alarm)} from "svelte-teenyicons";</script>
```

## Props

| Name                         | Default     |
| ---------------------------- | ----------- |
| size                         | 15          |
| class                        |             |
| ariaLabel                    | <file name> |
| variation (solid or outline) | outline     |

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

## aria-label

All icons have aria-label. For example `AbTesting` has `aria-label="ab testing"`.
Use `ariaLabel` prop to modify the `aria-label` value.

```html
<AbTesting ariaLabel="AB testing icon" class="text-red-500"></AbTesting>
```

## Passing down other attributes

You can pass other attibutes as well.

```html
<AbTesting tabindex="0"></AbTesting>
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
