---
slug: redpanda-console
id: u2fu9ivyspbt
type: challenge
title: Redpanda Topics
teaser: Learn how to create and consume topics.
notes:
- type: text
  contents: |
    # Creating a new topic

    To start building a basic streaming application, you can use `rpk` to create a topic, produce messages to it, and consume messages from it. rpk is a command-line tool for connecting to and interacting with Redpanda brokers.
tabs:
- title: Terminal
  type: terminal
  hostname: sandbox
- title: Redpanda console
  type: service
  hostname: sandbox
  port: 8080
difficulty: basic
timelimit: 600
---

🚀 Let's run it
===============

Now that you have created a topic from the CLI, lets explore from the Redpanda console.

👀 Step 01 - Redpanda Console tab
======================

Select the Redpanda Console tab (next the the terminal tab).

You should see the Redpanda Console.

An overview of the cluster status, cluster health, and broker details is displayed.

✅ Step 02 - Verifying messages
=================================

Go to Topics > chat-room.

The message that you produced to the topic is displayed along with some other details about the topic.

🏁 Finish
=========

Congratlations you have finished the Redpanda intro course.
