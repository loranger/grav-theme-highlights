# Highlights Theme

The **Highlights** Theme is for [Grav CMS](http://github.com/getgrav/grav).

## Description

[Highlights](https://html5up.net/highlights) port from [HTML5 UP](https://html5up.net/)

## Features

- Single page application
- Lightweight and minimal
- Fully responsive
- SCSS based CSS source files for easy customization
- Fontawesome icon support

### Supported Page Templates

- Default view template `default.md`

- Modular view templates:

  ```
  modular.md
  ```

  - Header Modular view template `header.md`
  - Part Modular view template `part.md`

# Installation

Installing the Highlights theme can be done in one of two ways. Our GPM  (Grav Package Manager) installation method enables you to quickly and easily install the theme with a simple terminal command, while the  manual method enables you to do so via a zip file.

## GPM Installation (Preferred)

The simplest way to install this theme is via the [Grav Package Manager (GPM)](http://learn.getgrav.org/advanced/grav-gpm) through your system's Terminal (also called the command line).  From the root of your Grav install type:

```shell
bin/gpm install highlights
```

This will install the Quark theme into your `/user/themes` directory within Grav. Its files can be found under `/your/site/grav/user/themes/highlights`.

## Manual Installation

To install this theme, just download the zip version of this repository and unzip it under `/your/site/grav/user/themes`. Then, rename the folder to `highlights`. You can find these files either on [GitHub](https://github.com/loranger/grav-theme-highlights) or via [GetGrav.org](http://getgrav.org/downloads/themes).

You should now have all the theme files under

```
/your/site/grav/user/themes/highlights
```

## Default Options

Highlights comes with a few default options that can be set site-wide.  These options are:

```yaml
enabled: true                 # Enable the theme
logo_image:                   # A custom logo to use as favicon
background_image:             # A custom image to use as the default background image
```

To make modifications, you can copy the `user/themes/highlights/highlights.yaml` file to `user/config/themes/` folder and modify, or you can use the admin plugin.

> NOTE: Do not modify the `user/themes/highlights/highlights.yaml` file directly or your changes will be lost with any updates

## Logo image

To add a custom logo, you should put the log into the `user/themes/highlights/images/logo` folder.  Standard image formats are support (`.png`,`.jpg`, `.gif`, `.svg`, etc.).  Then reference the logo via the YAML like so:

```yaml
logo_image:
    - name: 'my-logo.png'
```

Alternatively, you can you use the drag-n-drop "Logo image" field in the Highlights theme options.

## Background image

To add a custom background image, you should put the log into the `user/themes/highlights/images/background` folder.  Standard image formats are support (`.png`,`.jpg`, `.gif`, `.svg`, etc.).  Then reference the logo via the YAML like so:

```yaml
background_image:
    - name: 'my-background.png'
```

Alternatively, you can you use the drag-n-drop "Background image" field in the Highlights theme options.

# Pages

## Modular page

As a single page theme, the modular page is the default one. Once you create your modular page, you should add modular content children : One header and one or more parts.

## Header Modular Options

You can customize your header part with choosing to display or not a *begin* button leading to the first part of your single page website. You can also specify the label of this button

```yaml
display_button: true
button_label: Begin
```

## Part Modular Options

Each part of your single page website is a part page which can have a custom background, a displayed title or not, a custom next button label, and an ability to render list as grids

```yaml
display_title: true
next_label: Next
list_as_grid: false
background_image: mypic.jpg
```

## Default page

You can also use a default grav structure with pages using *default* template. A minimal navigation bar will be included and your content will be rendered as one single page.

## Default page Options

Each page can override the default website background image. The first uploaded image found in the page's folder will be used as background, but you can also specify another one if you uploaded more than one.

```yaml
background_image: 'image_name'
```

# Customization

Highlight is build with [Laravel-mix](https://laravel-mix.com) on top of [webpack](https://webpack.js.org/). You can install it and customize javascript and css using npm command prompt :

```shell
npm install
```

You can bundle your assets (defined in `webpack.mix.js`) using npm too.

```shell
npm run dev
```

builds you assets for development purpose

```shell
npm run production
```

bundles your assets for production.
