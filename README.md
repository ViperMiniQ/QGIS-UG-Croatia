# 🌐 QGIS User Group Croatia Website

> Source of the **QGIS User Group Croatia** (QGIS zajednica u Hrvatskoj) website, published at [hr.qgis.org](https://hr.qgis.org/).
>
> The site is built with [Hugo](https://gohugo.io/) and the [QGIS website theme](https://github.com/qgis/QGIS-Hugo-Website-Theme). It is based on the [QGIS User Group Website template](https://github.com/qgis/QGIS-User-Group-Website).

![-----------------------------------------------------](./img/green-gradient.png)

<!-- TABLE OF CONTENTS -->
<h2 id="table-of-contents"> 📖 Table of Contents</h2>

<details open="open">
  <summary>Table of Contents</summary>
  <ol>
    <li><a href="#-getting-started"> 🎯 Getting Started </a></li>
    <li><a href="#-folder-structure"> 📂 Folder Structure </a></li>
    <li><a href="#️-editing-the-site"> ✏️ Editing the Site </a></li>
    <li><a href="#-deployment"> 🚀 Deployment </a></li>
    <li><a href="#-license"> 📜 License </a></li>
    <li><a href="#-using-the-nix-shell"> 🧊 Using the Nix Shell </a></li>
    <li><a href="#-contributing"> ✨ Contributing </a></li>
  </ol>
</details>

![-----------------------------------------------------](./img/green-gradient.png)

## 🎯 Getting Started

### Prerequisites

- Hugo extended (version 0.139.0 or higher)
- Git
- A text editor or an IDE (eg. VSCode)

### Local Development

1. **Clone this repository:**
   ```bash
   git clone https://github.com/qgis/QGIS-UG-Croatia.git
   cd QGIS-UG-Croatia
   ```

2. **Install the QGIS website theme submodule:**
   ```bash
   git submodule update --init --recursive
   ```

3. **Run the development server:**
   ```bash
   make hugo-run-dev
   ```
   Or directly with Hugo:
   ```bash
   hugo server --config config.toml,config/config.dev.toml
   ```

4. **View the site:**
   Open your browser to `http://localhost:1313`

![-----------------------------------------------------](./img/green-gradient.png)

## 📂 Folder Structure

```plaintext
QGIS-UG-Croatia/
  ├── ⚙️  config/           # Hugo configuration files
  ├── 📄  content/          # Markdown content files (pages, posts)
  ├── 🧩  layouts/          # Hugo templates and partials
  ├── 📦  public/           # Generated site output (after `hugo` build)
  ├── 🗂️  resources/        # Hugo-generated resources (e.g., minified assets)
  ├── 📄  static/           # Static files served as-is (e.g., favicon, images, documents)
  ├── 🎨  themes/           # Hugo themes
  ├── ⚙️  config.toml       # Main Hugo configuration file
  ├── 🤝  CONTRIBUTING.md   # Contribution guidelines
  ├── 📜  LICENSE           # Project license
  ├── ⚙️  Makefile          # Build/Deployment automation commands
  └── 📖  README.md         # This file
```

![-----------------------------------------------------](./img/green-gradient.png)

## ✏️ Editing the Site

### Content Pages

All content is in the `content/` directory:

- `_index.md` - Home page (Početna)
- `about.md` - About us (O nama)
- `join-us.md` - Join us (Pridruži se)
- `donate.md`, `donate-instructions.md` - Donations (Doniraj)
- `rules.md` - Rules (Pravila)
- `dokumenti.md` - Association documents (Dokumenti); the PDFs live in `static/documents/`
- `events.md`, `community.md`, `case-studies.md`, `tutorials.md`, `blog/` - Other pages

Site content is written in Croatian. The files use Markdown with Hugo shortcodes.

### Configuration

Edit `config.toml` to change:

- Site title and URL
- Menu structure
- Colors and branding
- Analytics settings

### Navigation menu

The header menu is defined by the `[[menu.main]]` entries in `config.toml` and rendered by `layouts/partials/contextmenu.html`. The "Vanjske poveznice" entry mirrors the qgis.org top navigation as a dropdown.

### Images and Assets

- Place images in `static/img/` or `content/`
- Hero images are set in page front matter

### Styling

The site uses the `qgis-website-theme` which provides:

- Responsive design
- Clean, modern look
- Customizable colors
- Reusable content blocks

Colors and fonts can be customized in `config.toml` under `[params]`. Site-specific style overrides live in `assets/sass/custom.sass`.

![-----------------------------------------------------](./img/green-gradient.png)

## 🚀 Deployment

- **Production:** [hr.qgis.org](https://hr.qgis.org/) is built with `make build` (using `config/config.prod.toml`) and updated with `make deploy`. `make revert-deploy` restores the previous build.
- **Staging:** every push to `main` is built and deployed to GitHub Pages by `.github/workflows/github-pages.yml`.

![-----------------------------------------------------](./img/green-gradient.png)

## 📜 License

This project is licensed under the MIT License. See the [LICENSE](./LICENSE) file for details.

![-----------------------------------------------------](./img/green-gradient.png)

## 🧊 Using the Nix Shell

Please refer to the [Nix section](./CONTRIBUTING.md#nix) in [CONTRIBUTING.md](./CONTRIBUTING.md).

![-----------------------------------------------------](./img/green-gradient.png)

## ✨ Contributing

Fixes and improvements are welcome! Open an [issue](https://github.com/qgis/QGIS-UG-Croatia/issues) or submit a pull request to the `main` branch.

Please read the [CONTRIBUTING.md](CONTRIBUTING.md) for guidelines.

![-----------------------------------------------------](./img/green-gradient.png)

## 🙋 Have Questions?

- **Website questions:** Open an issue in this repository
- **General QGIS questions:** Visit [qgis.org](https://qgis.org)

![-----------------------------------------------------](./img/green-gradient.png)

## 🧑‍💻👩‍💻 Contributors

- [Tim Sutton](https://github.com/timlinux) – Original QGIS Website author
- [Lova Andriarimalala](https://github.com/Xpirix) – User Group website template developer
- [QGIS Contributors](https://github.com/qgis/QGIS-UG-Croatia/graphs/contributors) – Community contributors

Made with ❤️ by the QGIS Contributors.
