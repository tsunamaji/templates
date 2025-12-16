# tsunamaji/templates

The repository contains various starter kits and templates. It provides starting points in different combinations from open-source creators listed in the credits.

## How to use it

For cloning from GitHub:
```none
git clone --depth 1 --filter=blob:none --sparse https://github.com/tsunamaji/templates.git
cd templates
git sparse-checkout set {template_name}
```

StackBlitz for running quick examples:
```none
https://stackblitz.com/github/tsunamaji/templates/{template_name}
```

## Tools

For space efficiency, we use `pnpm`. All commands here can also be run with `npm`.

### Vite

For any Vite bundler-based project, use the following command:

```none
pnpm create vite@latest
```

References:
* https://vite.dev/guide/#scaffolding-your-first-vite-project

### Sass

In most cases, only the Sass dependency needs to be installed:

```none
pnpm i -D sass@1
```

References:
* https://sass-lang.com/install/#install-npm

### TailwindCSS

In v4, we can already rely on a Vite plugin:
```none
pnpm i -D tailwindcss@4 @tailwindcss/vite
```

In v3, PostCSS is required in any case:
```none
pnpm i -D tailwindcss@3 postcss autoprefixer
```

References:
* https://tailwindcss.com/docs/installation/using-vite
* https://v3.tailwindcss.com/docs/installation/using-postcss

## Structure

Instead of many subfolders, each template is given a long folder name, for example: `vite-v7-vue-v3-sass-v1-tailwindcss-v4`. First, always list the bundlers, then the JS framework, followed by everything else. For instance, PostCSS or LightningCSS are not listed because their installation is not required - they are considered extra dependencies. The projects can be created with a few command-line commands, but to understand their structure, a ready-made illustrative example is necessary. This illustrative example can be found inside each folder.

## License

Copyright (C) 2025–present [Zoltán Rózsa](https://github.com/rozsazoltan) & [Tsunamaji](https://github.com/tsunamaji)

This version is licensed under the MIT.  
For full license terms, see the [LICENSE](./LICENSE) file.

## Credits

This project is made possible by much love and the other open source software.

| Name                                                                    | License                                                               |
| :---------------------------------------------------------------------- | :-------------------------------------------------------------------- |
| [tailwindlabs/tailwindcss](https://github.com/tailwindlabs/tailwindcss) | MIT License © [Tailwind Labs, Inc.](https://github.com/tailwindlabs)  |
| [vitejs/vite](https://github.com/vitejs/vite)                           | MIT License © [VoidZero Inc.](https://github.comvoidzero)             |
| [vuejs/vue](https://github.com/vuejs/vue)                               | MIT License © [Yuxi (Evan) You](https://github.com/yyx990803)         |
| [facebook/react](https://github.com/facebook/react)                     | MIT License © [Meta Platforms, Inc.](https://github.com/facebook)     |
| [sass/dart-sass](https://github.com/sass/dart-sass)                     | MIT License © [Google Inc.](https://github.com/google)                |

## Thanks

A special thanks to all contributors of the open-source projects used in this repository. Your work, dedication, and commitment to maintaining and distributing these tools as open source make projects like this possible.

**Motivation:** Because _together_, nothing is impossible.
