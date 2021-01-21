# Splittable

## Goal

This gem solves the problem of several decimal places in divisions where the result must be presented in cents, that is converting the division result to only two decimal places and the difference is attributed to the first plot.

## Installation

Add this line to your application's Gemfile:

```ruby
gem 'splittable'
```

And then execute:

    $ bundle install

Or install it yourself as:

    $ gem install splittable

## Usage

Using `division` method:

``` ruby
Splittable.division(value: 0.1188888, quantity: 3)
```

Result: the total truncated value was divided by the number of plots informed and attributed the difference in the first installment:

```ruby
=> [0.5e-1, 0.3e-1, 0.3e-1] # => [0.05, 0.03, 0.03]
```

Using `normalize` method:

```ruby
Splittable.normalize(value: 100.003, installments: [33.33, 21.433, 43.33333])
```

Result: all values are truncated and them the difference is attributed in the first installment:

```ruby
=> [0.3524e2, 0.2143e2, 0.4333e2] # => [35.24, 21.43, 43.33]
```

## Development

After checking out the repo, run `bin/setup` to install dependencies. Then, run `rspec` to run the tests. You can also run `bin/console` for an interactive prompt that will allow you to experiment.

To install this gem onto your local machine, run `bundle exec rake install`. To release a new version, update the version number in `version.rb`, and then run `bundle exec rake release`, which will create a git tag for the version, push git commits and tags, and push the `.gem` file to [rubygems.org](https://rubygems.org).

## Contributing

Bug reports and pull requests are welcome on GitHub at https://github.com/Pagnet/splittable/blob/master/CONTRIBUTING.md.

## Code of Conduct

Welcome on GitHub at https://github.com/Pagnet/splittable/blob/master/CODE_OF_CONDUCT.md.
