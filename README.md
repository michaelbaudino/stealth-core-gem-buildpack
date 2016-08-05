# Heroku buildpack for silently installing Kyero core gem

This buildpack is intended for use after the regular [ruby-buildpack].

# Usage

If you are using the default buildpack, manually set your buildpack to Heroku's default Ruby buidlpack

```
heroku buildpacks:set heroku/ruby
```

Append the buildpack-ruby-rake-deploy-tasks to your buildpack list:

```
heroku buildpacks:add https://github.com/michaelbaudino/stealth-core-gem-buildpack
```

Configure BUNDLE_GEM__FURY__IO environment variable with the tasks you want to run:

```
heroku config:set BUNDLE_GEM__FURY__IO='YoUr_GemFury_PerSoNal_Token'
```

# License

MIT, see the LICENSE file.

[ruby-buildpack]:https://github.com/heroku/heroku-buildpack-ruby
