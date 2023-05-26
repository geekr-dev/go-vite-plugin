# Go Vite Plugin

## Introduction

[Vite](https://vitejs.dev) is a modern frontend build tool that provides an extremely fast development environment and bundles your code for production.

This plugin configures Vite for use with a Go backend server.

## Usage

install:

```
npm i go-vite-plugin
```

config in the `vite.config.js`:

```
import { defineConfig } from 'vite';
import go from 'go-vite-plugin';
import vue from '@vitejs/plugin-vue';

export default defineConfig({
    plugins: [
        go({
            input: 'resources/js/app.js',
            refresh: true,
        }),
        vue({
            template: {
                transformAssetUrls: {
                    base: null,
                    includeAbsolute: false,
                },
            },
        }),
    ]
});
```

## License

The Go Vite plugin is open-sourced software licensed under the [MIT license](LICENSE.md).
