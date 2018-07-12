# Jekyll::Paginate::Category

[![Gem Version](https://badge.fury.io/rb/jekyll-paginate-category.svg)](http://badge.fury.io/rb/jekyll-paginate-category)
[![Dependency Status](https://gemnasium.com/midnightSuyama/jekyll-paginate-category.svg)](https://gemnasium.com/midnightSuyama/jekyll-paginate-category)

Pagination Generator for Jekyll Category

## Installation

Add this line to your application's Gemfile:

```ruby
gem 'jekyll-paginate-category'
```

And then execute:

    $ bundle

Or install it yourself as:

    $ gem install jekyll-paginate-category

## Usage

### _config.yml

```yaml
gems: [jekyll-paginate, jekyll-paginate-category]

paginate: 5
paginate_path: "page:num"

category_dir: "categories"
category_layout: "index.html"
```

### index.html (category_layout)

```html
{% if page.paginator %}
{% assign paginator = page.paginator %}
{% endif %}

{% for post in paginator.posts %}
...
{% endfor %}
```

## Simple how-to

This plugin is designed to generate paginated categories for your jekyll project. If you've added categories to the YAML front matter for your posts, the only files you should need to change are your `_config.yml` and `index.html` files.

Change these files as indicated below, then build your project. A set of paginated category pages will be generated in your `_site` folder, in the folder you specify in `category_dir`. The structure of these will be based on your `index.html` file, and the page.title for each will be the name of the category. These will then be accessible at e.g. /categories/mycategory.

## Development

After checking out the repo, run `bin/setup` to install dependencies. Then, run `rake false` to run the tests. You can also run `bin/console` for an interactive prompt that will allow you to experiment.

To install this gem onto your local machine, run `bundle exec rake install`. To release a new version, update the version number in `version.rb`, and then run `bundle exec rake release`, which will create a git tag for the version, push git commits and tags, and push the `.gem` file to [rubygems.org](https://rubygems.org).

## Contributing

Bug reports and pull requests are welcome on GitHub at https://github.com/midnightSuyama/jekyll-paginate-category. This project is intended to be a safe, welcoming space for collaboration, and contributors are expected to adhere to the [Contributor Covenant](contributor-covenant.org) code of conduct.


## License

The gem is available as open source under the terms of the [MIT License](http://opensource.org/licenses/MIT).

