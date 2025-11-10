# WSPR Beakon Documentation Website

This is the official documentation website for WSPR Beakon, an open-source WSPR (Weak Signal Propagation Reporter) beacon transmitter built with ESP32 and Si5351 modules. The site provides complete technical documentation, assembly guides, software configuration, and component specifications.

Live Website: **[Visit the Documentation](https://danielcharrua.github.io/wspr-beakon-docs/)**

Available Languages:

- English (default)
- Español - Complete Spanish translation

## Development Setup

### Prerequisites

- Node.js (v16 or higher)
- Yarn package manager

### Installation

```bash
yarn install
```

### Local Development

Start the development server (English):
```bash
yarn run start
```

Start with Spanish locale:
```bash
yarn run start --locale es
```

The development server opens at `http://localhost:3000` with live reload for most changes.

### Building for Production

```bash
yarn build
```

Generates static content in the `build` directory ready for deployment to any static hosting service.

### Adding Translations

Generate translation files:
```bash
yarn write-translations --locale fr
```

### Deployment to GitHub Pages (Automatic)

Using SSH (recommended):
```bash
USE_SSH=true yarn deploy
```

Using HTTPS:
```bash
GIT_USER=<Your GitHub username> yarn deploy
```

This builds the website and pushes to the `gh-pages` branch for automatic GitHub Pages deployment.

### Manual Deployment

After running `yarn build`, deploy the `build` directory contents to any static hosting provider.

## License

Documentation content is provided under the same license as the WSPR Beakon project. See the main project repository for license details.

## Contributing

Contributions to improve the documentation are welcome! Please:

1. Fork this repository
2. Create a feature branch
3. Make your improvements
4. Submit a pull request

For technical issues with the WSPR Beakon hardware or firmware, please use the [main project repository](https://github.com/danielcharrua/wspr-beakon).
