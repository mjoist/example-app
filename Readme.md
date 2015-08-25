# Karafka example

This is test application which uses karafka gem to receive messages from Kafka server
and waterdrop gem to send messages to Kafka server.

To run this application locally you should run kafka and zookeeper servers on those hosts and ports which
are set in *app.rb* and */config/initializers/water_drop.rb* files.

## Usage

The next tasks are available. You should run them in the console.

#### Run sidekiq worker to manage perform methods of controllers
```
  bundle exec rake karafka:sidekiq
```
#### Run Kafka consumer. It will receive messages and send them to needed controller based on it's topic name
```
  bundle exec rake karafka:run
```

#### Generate messages to Kafka server in two ways: by applying aspects to methods, and by sending message directly.

```
  bundle exec rake waterdrop:send
```
