# Event Driven Architecture

## What’s the difference between a FIFO and a standard queue?

The FIFO queue follows the first in first out approach. It emits events in order and make sure that no event surpasses the other. While standered queue does not care about the order in which events are emitted. Therefore, events can be emitted on whatever order is more suitable for the server.

## How can the server be assured a message was properly received?

It will recive a feedback from the client that the event and the message was received and the handler applied. These are attained by using socket.io acknowledgement.

## What classic design pattern is best represented by event driven programming?

The Observer Design Pattern, define a one-to-many dependency between objects so that when one object changes state, all its dependents are notified and updated automatically.
Encapsulate the core (or common or engine) components in a Subject abstraction, and the variable (or optional or user interface) components in an Observer hierarchy.
The "View" part of Model-View-Controller.

## How do you test an event driven system?

Using jest we can mock some event emits and test against event handlers. If we receive an acknowledgement from the client, the test will pass, otherwise it needs fixes.

## Terms

### FIFO Queue

First In First Out method sorts the assets in order of their enrollment in the structure. Assets can only be used/sent/removed in order, the oldest is affected first.

### Pub/Sub

Publish/Subscribe architecture is not based on who is publishing or who has subscribed to receive messages. Messages are categorized into classes.
Publishers label their messages with the proper class. Subscribers receive messages depending on the classes they prefer regardless of who is publishing them.
