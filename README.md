# Shopify Bones

Shopify Bones is a base Shopify theme designed for creating themes from scratch. If you're looking for a stripped down liquid skeleton with lean semantic markup, this is it. No comments, no classes. Includes customer area.

# Getting Started

Shopify Bones has a few dependencies but it doesn't actually make use of any them. These include libraries such as Foundation, but you can use your favorite grid. See `bower.json` and `Gemfile` for more details.

Make sure you have bundler and bower installed:

    gem install bundler && npm install -g bower

Then run:

    bundle install && bower install

### Configure your Shopify store

The `shopify_theme` gem is built-in. Rename `config.sample.yml` to `config.yml` and configure for your particular shop. See [shopify_theme][3] for details.

### Using Guard

Shopify Bones uses [guard][1] to watch files and manage assets. To run it, type:

    guard

Guard will:

- Concatenate and minify script files in `source/javascripts` to `assets/shop.js`
- Compile Sass files in `source/stylesheets` to `assets/shop.scss.liquid`
- Automatically compress new images in the assets directory
- Automatically push theme changes to your shop using the shopify theme gem if it sees a config.yml file

It does all of this conveniently in a single terminal window. See the `Guardfile`.

### Binary Dependencies for Compressing Images

Guard uses the `image_optim` gem to compress images. It relies on a few [binary dependencies][2] that you might be missing. Those can be installed easily with homebrew.


[1]: https://github.com/guard/guard
[2]: https://github.com/toy/image_optim#binaries-installation
[3]: https;//github.com/shopify/shopify_theme
