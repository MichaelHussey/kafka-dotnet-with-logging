### kafka-dotnet-with-logging

Example showing how to enable detailed librdkafka logging in Confluent's dotnet client

Based on this sample from the Confluent Kafka .NET - https://github.com/confluentinc/confluent-kafka-dotnet/tree/master/examples/Configuration

Build the program

`docker build -t kafakdotnet .`

Run the program
`docker run -it --rm --name kdn kafakdotnet`

## How it works

The "Debug" property in the consumer and producer property sets is passed through to the underlying librdkafka library. This should contain a list of possible logging items/events that is understood by librdkafka. For a full list of possible values see https://github.com/confluentinc/librdkafka/blob/master/INTRODUCTION.md#debug-contexts

Confluent Support portal also has a useful Knowledge Base article:  https://support.confluent.io/hc/en-us/articles/19562024268052-How-to-set-up-logging-in-librdkafka-C-NET

