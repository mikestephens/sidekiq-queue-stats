# Sidekiq::QueueStats [![Build Status](https://travis-ci.org/mikestephens/sidekiq-queue-stats.svg?branch=master)](https://travis-ci.org/mikestephens/sidekiq-queue-stats)

Keeps track of Sidekiq job count and adds a tab to the Web UI to let you view totals.

## Installation

Add this line to your application's Gemfile:

```ruby
gem 'sidekiq-queue-stats'
```

## Usage

Simply having the gem in your Gemfile is enough to get you started. Your
job count will be visible via a Queue Stats tab in the Web UI.

![Web UI](http://i.imgur.com/eSNVK0O.png)

### Configuration

Add this block to `config/initializers/sidekiq.rb`

```
Sidekiq::QueueStats.configure do |config|
  config.max_limit = 50000
end
```

#### Max Limit

Iterating through large queues can be resource intensive and take quite a lot of time. This option lets you set an integer to only show queue stats of queues under a pre defined threashold.

## Dependencies

Depends on Sidekiq >= 2.16.0

## Contributing

1. Fork it
2. Create your feature branch (`git checkout -b my-new-feature`)
3. Commit your changes (`git commit -am 'Added some feature'`)
4. Push to the branch (`git push origin my-new-feature`)
5. Create new Pull Request

## License

Released under the MIT License. See the [LICENSE][license] file for further details.

[license]: https://github.com/mhfs/sidekiq-queue-count/blob/master/LICENSE
