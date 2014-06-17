## Shopify Bones

Shopify Bones is a base Shopify theme designed for creating themes from scratch. If you're looking for a stripped down liquid skeleton with lean semantic markup, this is it. No comments, no classes. Includes customer area. Foundation 5 grid dropped in for convenience.

## Getting Started

First, make sure you have bundler and bower installed:

    gem install bundler && npm install -g bower

Then do:

    bundle install && bower install

To install dependencies.

## Guard

Shopify Bones uses [guard][1] to watch files and manage assets. To run it, type:

    guard

Guard will:

- Concatenate and minify script files in `source/javascripts` to `assets/shop.js`
- Compile Sass files in `source/stylesheets` to `assets/shop.scss.liquid`
- Compresses images that are dropped into the assets directory
- Keeps your theme in sync using the shopify theme gem

It does all of this in a single terminal window. See the `Guardfile` for more details.

[1]: https://github.com/guard/guard
