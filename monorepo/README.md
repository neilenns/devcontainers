# Monorepo devcontainer

Devcontainer for monorepo development, based around pnpm and turborepo.

## Usage

```json
"image": "ghcr.io/neilenns/devcontainers/monorepo:latest"
```

Also, copy the `post-create.sh` file to your `.devcontainer` folder. This will run after the container is created, and is used to install any additional tools.

## Installed features

- Gitleaks
- oh-my-zsh, with auto-update, workspaces/ stripped from the prompt, and agnoster for the theme
- Pre-commit
- Python
- Shell history
- [Safe-chain](https://github.com/AikidoSec/safe-chain)

## Installed vscode extensions

- File nesting
- Github actions
- Jock SVG
- Markdown all-in-one
- Markdown footnote
- Markdownlint
- Mongodb
- Nanoid generator
- oklch preview
- oklchanger
- pnpm
- Postcss
- prettier
- Remote containers
- Spell checker
- Tailwind css
