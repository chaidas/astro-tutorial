# Astro Starter Kit: Minimal

2025-04-27: Playing around with `npm create astro` and v5.7.5

## Notes

- Initiated using `npm create astro@latest -- --template minimal`
- Remember: Any JS written in a component's frontmatter is run _at build time_

### Prettier setup

Added Prettier with `npm i --save-dev prettier prettier-plugin-astro` and then added the `prettier` key on `package.json`:

```json
{
    "prettier": {
        "tabWidth": 4,
        "plugins": ["prettier-plugin-astro"]
    }
}
```

Note that "plugins" was needed in order for webstorm to be able to format on CMD+SHIFT+OPT+P correctly `.astro` files.

## Project Structure

Inside of your Astro project, you'll see the following folders and files:

```text
/
├── public/
├── src/
│   └── pages/
│       └── index.astro
└── package.json
```

Astro looks for `.astro` or `.md` files in the `src/pages/` directory. Each page is exposed as a route based on its file name.

There's nothing special about `src/components/`, but that's where we like to put any Astro/React/Vue/Svelte/Preact components.

Any static assets, like images, can be placed in the `public/` directory.

## Commands

All commands are run from the root of the project, from a terminal:

| Command                   | Action                                           |
| :------------------------ | :----------------------------------------------- |
| `npm install`             | Installs dependencies                            |
| `npm run dev`             | Starts local dev server at `localhost:4321`      |
| `npm run build`           | Build your production site to `./dist/`          |
| `npm run preview`         | Preview your build locally, before deploying     |
| `npm run astro ...`       | Run CLI commands like `astro add`, `astro check` |
| `npm run astro -- --help` | Get help using the Astro CLI                     |

## Common Conventions (But Not Required)
There are no enforced naming conventions for folders inside `/src` except for the reserved `pages` and `content` directories. 
Astro recommends, but does not require, several other folder names inside `/src` for organizational clarity:
- `src/components/`: For reusable UI components (Astro, React, Vue, etc.).
- `src/layouts/`: For layout components that define shared UI structures.
- `src/styles/`: For CSS, Sass, or other style files.
- `src/images/` or `src/assets/`: For images or other asset files you want Astro to process and optimize.
- `src/scripts`: For client-side JS
