## Sensu-Plugins-rabbitmq

[![Build Status](https://travis-ci.org/sensu-plugins/sensu-plugins-rabbitmq.svg?branch=master)](https://travis-ci.org/sensu-plugins/sensu-plugins-rabbitmq)
[![Gem Version](https://badge.fury.io/rb/sensu-plugins-rabbitmq.svg)](http://badge.fury.io/rb/sensu-plugins-rabbitmq)
[![Code Climate](https://codeclimate.com/github/sensu-plugins/sensu-plugins-rabbitmq/badges/gpa.svg)](https://codeclimate.com/github/sensu-plugins/sensu-plugins-rabbitmq)
[![Test Coverage](https://codeclimate.com/github/sensu-plugins/sensu-plugins-rabbitmq/badges/coverage.svg)](https://codeclimate.com/github/sensu-plugins/sensu-plugins-rabbitmq)
[![Dependency Status](https://gemnasium.com/sensu-plugins/sensu-plugins-rabbitmq.svg)](https://gemnasium.com/sensu-plugins/sensu-plugins-rabbitmq)

## Functionality

## Files
 * bin/check-rabbitmq-alive.rb
 * bin/check-rabbitmq-amqp-alive.rb
 * bin/check-rabbitmq-cluster-health.rb
 * bin/check-rabbitmq-consumers.rb
 * bin/check-rabbitmq-messages.rb
 * bin/check-rabbitmq-network-partitions.rb
 * bin/check-rabbitmq-node-health.rb
 * bin/check-rabbitmq-node-usage.rb
 * bin/check-rabbitmq-queue-drain-time.rb
 * bin/check-rabbitmq-queue.rb
 * bin/check-rabbitmq-queues-synchronised.rb
 * bin/check-rabbitmq-stomp-alive.rb
 * bin/metrics-rabbitmq-overview.rb
 * bin/metrics-rabbitmq-queue.rb
 * bin/metrics-rabbitmq-exchange.rb

## Usage

## Installation

[Installation and Setup](http://sensu-plugins.io/docs/installation_instructions.html)

## Permissions

In order to run these checks you need the following permissions set:
```
:conf => '^aliveness-test$',
:write => '^amq\.default$',
:read => '.*'
```
You must also add the `monitoring` tag.

This can be done like this:
```
rabbitmqctl add_user sensu_monitoring $MY_SUPER_LONG_SECURE_PASSWORD
rabbitmqctl set_permissions  -p / sensu_monitoring "^aliveness-test$" "^amq\.default$" "^(amq\.default|aliveness-test)$"
rabbitmqctl set_user_tags sensu_monitoring monitoring
```

**It is highly recommended that you do not give administrator access! and use minimum permissions!**

## Notes
