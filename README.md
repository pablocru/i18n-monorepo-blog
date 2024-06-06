# i18n Monorepo Blog

A monorepo to manage a blog with internationalization (i18n) across two separate projects,
allowing each one to be deployed on its own domain or subdomain. This approach ensures
control over the content published in each language, rather than relying on a translation
plugin.

## Project structure

This project has the following structure:

```txt
|- i18n-monorepo-blog
|  |- packages
|  |  |- components
|  |  |- layouts
|  |  |- websites
```

Even though there are 3 folders inside `packages`, there are actually 2 types:

- [Astro component](https://docs.astro.build/en/reference/publish-to-npm/)
  - `components`
  - `layouts`
- Astro project
  - `websites`

The main deference is that an Astro project is a website by its own and an Astro component
is a library that must be installed in an Astro project.

## Create an Astro component

To create an Astro component you must use the `component` template:

```bash
npm create astro@latest "<component-name>" -- --template component
```

```bash
npm create [...] --install --no-git --typescript strict --template component
```

## Install a local Astro component

I use the following command in the `website` that I want to install an Astro component:

```bash
npm install "@<folder-name>/<component-name>"
```

## Bugs or suggestions

If you found a bug or have a suggestion please don't hesitate to contact me or open an
[issue on GitHub](https://github.com/pablocru/i18n-monorepo-blog/issues).
