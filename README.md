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
            input: 'resources/js/app.js',  // js source code entry point
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

when you run `npm run dev`, then you can visit `http://localhost:5173` in your browser:

![go-vite-plugin](https://github.com/geekr-dev/go-vite-plugin/assets/114386672/15e93bf8-5784-4d63-a326-16332c630e7f)

## License

The Go Vite plugin is open-sourced software licensed under the [MIT license](LICENSE.md).
