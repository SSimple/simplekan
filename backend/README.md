# SimpleKan
[![Code Climate](https://codeclimate.com/github/victormilitao/simplekan/badges/gpa.svg)](https://codeclimate.com/github/victormilitao/simplekan)

[![Test Coverage](https://codeclimate.com/github/victormilitao/simplekan/badges/coverage.svg)](https://codeclimate.com/github/victormilitao/simplekan/coverage)

Backend of SimpleKan

This app uses Rails 4.2.5 and Ruby 2.2.3

## Installing
Before installing, dont forget to install postgres

```console
sudo apt-get install postgresql postgresql-contrib libpq-dev
```

And to have newer version of node then install bower

npm install -g bower

Now to installation


```console
git clone git@github.com:victormilitao/simplekan.git
cp config/database.yml.example config/database.yml
cp config/application.yml.example config/application.yml
bundle install
bundle exec rake db:setup
rake db:test:prepare
```

## ERRORS

An error occurred while installing [capybara-webkit](https://github.com/thoughtbot/capybara-webkit/issues/707) (1.7.1), and Bundler cannot continue.
Make sure that `gem install capybara-webkit -v '1.7.1'` succeeds before bundling.

How to resolve:

```
sudo apt-get update && sudo apt-get install libqt5webkit5-dev qtdeclarative5-dev
```

## PhantomJS

[Install PhantomJS](http://phantomjs.org/build.html)

```
sudo apt-get install phantomjs
```

## Before commiting your code

### Use pre-commit gem

Please read https://github.com/jish/pre-commit

```console
  gem install pre-commit
```

Our default pre-commit is:

```console
  git config pre-commit.checks "whitespace, pry, yaml, json, before_all, merge_conflict, ruby_symbol_hashrockets, tabs, white_space"
```

# Testing

This app uses Rspec and [Factory Girl](https://github.com/thoughtbot/factory_girl).

Please read [betterspecs.org](http://betterspecs.org/).

Running with [Guard](https://github.com/guard/guard-rspec):

```console
bundle exec guard
```
