+++
author = "John Wang"
title = "Glip Inbound Webhook SDKs"
date = "2016-02-09"
tags = [
    "chat"
]
url = "/glip/inbound-webhook-sdks/"
+++

I recently put together two SDKs to wrap Glip’s inbound webhooks when there’s a desire to have data from other sites integrated into Glip alerts.

I originally built the library as a [Ruby SDK](https://github.com/grokify/glip-poster-ruby) since this is one of my go-to languages for quick prototyping, however, after learning that many chat users may not be developers with the means to run their own servers, I looked into writing this as a Google App and a Swift iOS app. The Google App is still in development but the [Swift SDK](https://github.com/grokify/glip-sdk-swift) is out.

<!--more-->

## Use Cases

Chat systems like Glip and others are used to consolidate information into teams and private messages for easy consolidated reading via web clients and mobile clients. By enabling multiple services to write into these chat teams, more people can be alerted to important events.

The initial use cases I’ve implemented and discussed include the following:

* Posting new voicemails to chat teams
* Posting new inbound faxes to chat teams
* Posting new inbound SMS text to chat teams: request

## Ruby SDK

The Ruby SDK, [`Glip::Poster`](https://github.com/grokify/glip-poster-ruby) is designed to have the same interface as other *::Poster chat SDKs making them interchangeable. It provides an easy to use interface supporting webhook options on a per-message basis and as part of the defaults.

```ruby
require 'glip_poster'

poster = Glip::Poster.new(YOUR_WEBHOOK_URL)
poster.options[:icon] = 'http://example.com/icon.png'
poster.send_message('Hi there!')
```

As mentioned above, while Ruby is nice and used by many people, setting up a service to transform event data to Glip’s inbound webhook format requires standing up a server permanently which may not be attractive or possible given the circumstances.

## Swift SDK

When thinking of alternative approaches, the thought of creating a Chrome App and an iOS App both came up. When the iOS app was the only viable choice, the [Glip Swift SDK](https://github.com/grokify/glip-sdk-swift) was born.

```swift
glip = Poster(YOUR_WEBHOOK_URL, icon: "http://example.com/icon.png")
glip.sendMessage("Hi there!")
```

## SMS to Glip Webhook Example

In addition to the SDK libraries themselves, the Ruby SDK includes a sample script [`sms_to_chat.rb`](https://github.com/grokify/ringcentral-sdk-ruby/blob/master/scripts/sms_to_chat.rb) which runs and demonstrates this in action. As part of the solution, the script subscribes to all inbound extensions and will send an alert to the chat system of choice for new alerts.

## Summary

Although the Glip Inbound Webhook format is simple, create an easy to use SDK is still very helpful. If you have an interest in using Glip, please try out these SDKs and provide feedback.
