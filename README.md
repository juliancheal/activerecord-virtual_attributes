# VirtualAttributes

This allows you to define a ruby method that acts like an attribute or relation.

Sometimes you have a model with an attribute defined in ruby, but you want to sort by it or filter by it.
Well, to filter by that attribute, you need to fetch all the rows from the database and filter it in ruby.
For large tables, this is slow and takes up a lot of memory

This gem allows you to represent these attribute in sql so `ORDER BY` `WHERE` clauses will work.

This gem also allows you to calculate counts, and treat those counts as a field accessible with `select(:child_count)`
to get rid of the N+1 problem of running a `count(*)` on a subcollection for each row.

## Installation

Add this line to your application's Gemfile:

```ruby
gem 'activerecord-virtual_attributes'
```

And then execute:

    $ bundle

Or install it yourself as:

    $ gem install activerecord-virtual_attributes

## Usage

TODO: Write usage instructions here

## Development

After checking out the repo, run `bin/setup` to install dependencies. Then, run `rake spec` to run the tests. You can also run `bin/console` for an interactive prompt that will allow you to experiment.

To install this gem onto your local machine, run `bundle exec rake install`. To release a new version, update the version number in `version.rb`, and then run `bundle exec rake release`, which will create a git tag for the version, push git commits and tags, and push the `.gem` file to [rubygems.org](https://rubygems.org).

## Contributing

Bug reports and pull requests are welcome on GitHub at https://github.com/ManageIQ/activerecord-virtual_attributes .

## License

The gem is available as open source under the terms of the [MIT License](https://opensource.org/licenses/MIT).
