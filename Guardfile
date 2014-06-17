# /usr/bin/env ruby

require 'guard'

notification :off

guard 'sass', 
  input: 'source/stylesheets',
  output: 'assets',
  extension: ".scss.liquid",
  all_on_start: true,
  load_paths: ['./bower_components'],
  shallow: true,
  quiet: true,
  style: :compressed

guard 'sprockets',
  destination: 'assets',
  asset_paths: ['bower_components', 'source/javascripts', 'assets'],
  root_file: 'source/javascripts/shop.js',
  minify: true do
    watch %r{^source\/javascripts\/.+\.js}
  end
  
guard 'shell'  do
  watch %r{^assets\/.+(\.png|\.jpg|\.jpeg|\.gif)} do |image|
    `image_optim #{image[0]}`
  end
end

if File.exists?('config.yml')
  guard 'shell' do
    watch %r{^(assets|config|layout|snippets|templates)\/.*} do |m|
      File.exists?(m[0]) ? `theme upload #{m[0]}` : `theme remove #{m[0]}`
    end
  end
end