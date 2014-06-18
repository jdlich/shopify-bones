## Shopify Bones

Shopify Bones is a base Shopify theme designed for creating themes from scratch. If you're looking for a stripped down liquid skeleton with lean semantic markup, this is it. No comments, no classes. Includes customer area.

## Getting Started

First, make sure you have bundler and bower installed:

    gem install bundler && npm install -g bower

Then run:

    bundle install && bower install

To install dependencies.

#### Binary Dependencies for Compressing Images

The `image_optim` gem is used to compress new image assets. It relies on a few [binary dependencies][2] that you might be need to install with brew.

## Guard

Shopify Bones uses [guard][1] to watch files and manage assets. To run it, type:

    guard

Guard will:

- Concatenate and minify script files in `source/javascripts` to `assets/shop.js`
- Compile Sass files in `source/stylesheets` to `assets/shop.scss.liquid`
- Automatically compress new images in the assets directory
- Automatically push theme changes to your shop using the shopify theme gem if it sees a config.yml file

It does all of this conveniently in a single terminal window. See the `Guardfile`.

[1]: https://github.com/guard/guard
[2]: https://github.com/toy/image_optim#binaries-installation
