# Minimal SCSS

Minimal template for writing Discord themes in SCSS.

## License
This template is licensed under the [MIT License](https://github.com/MiniDiscordThemes/MinimalSCSS/blob/main/LICENSE).

Retaining the license is only required if you share or modify this to be used as a template by others. Your themes created using this template do not need to retain the license, and can use any license (or no license) as you wish.

## Usage
### Prerequisites

You will need the following installed:
1. [git](https://git-scm.com/downloads)
2. [pnpm](https://pnpm.io/installation)

### Setup
1. With this repository as a template, [create a new repository](https://github.com/new?template_name=MinimalSCSS&template_owner=MiniDiscordThemes) for your theme.
2. Clone your repo to your computer.
3. Run `pnpm i` to install the dependencies.

### Theme editing
Write the theme files inside the `scss` directory.
- Run `pnpm run watch` to compile human-readable CSS to the `dev` directory when changes are detected in `scss`.
- Run `pnpm run build` to compile compressed CSS to the `dist` directory.
  - Use this to preview the version that will be published on GitHub Pages.
- Run `pnpm run format` to tidy up formatting with Prettier.
  - The format can be [configured](https://prettier.io/docs/en/options.html) in `.prettierrc.json`.
  
#### Assets
Images and other assets to publish on GitHub Pages should be placed in the `asset` directory.

### Publishing
When your repo is pushed to GitHub, the "Build and deploy CSS" workflow will run automatically. This creates a `deploy` branch containing the compressed CSS and any theme assets.

For example, for a theme with the following structure on the `main` branch:

```
(main)
├── scss
│   └── main.scss
└── asset
    └── img
        └── icon.png
```

This will be the output on the `deploy` branch:

```
(deploy)
├── main.css
└── asset
    └── img
        └── icon.png
```

To publish the output on GitHub Pages, simply go to the repository's Settings > Pages, and select the `deploy` branch as the source.
