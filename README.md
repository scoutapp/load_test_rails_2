# Rails 2 Testing App for ScoutAPM

This is a test app to ensure ScoutAPM is compatible with Rails 2.3.18 and Ruby 1.9.3-p551.

## Bootstrap

Bundler is not used for this old-school app. To get going:

* gem install activerecord-postgresql-adapter
* rake gems:install db:create db:migrate db:seed

## Starting the app

SCOUT_KEY=YOUR_KEY script/server -p8080

## Troubleshooting

If you're seeing: `WARNING: 'require 'rake/rdoctask'' is deprecated.` or `undefined method `source_index' for Gem:Module`, it's probably because you have a version of rubygems that's too new. Check it with `gem --version`, and if it's newer than 2.0, update with:

    gem update --system 1.8.25
