---
slug: redpanda-cli
id: xmtaifbmieyv
type: challenge
title: Redpanda CLI
teaser: Learn the basics of the Redpanda `rpk` CLI
notes:
- type: text
  contents: |
    # Learn about the Redpanda CLI

    In this first challenge, you will become familiar with the Redpanda `rpk` command-line tool (CLI).

    Redpanda `rpk` facilitates connecting to and interacting with Redpanda brokers.

    The `rpk` CLI comes pre-installed with every Redpanda broker, so you can use it inside one of the Redpanda Docker containers, or you can install it on your local machine to test connectivity.
tabs:
- title: Terminal
  type: terminal
  hostname: sandbox
difficulty: basic
timelimit: 600
---

🧪 Cluster Information
=======================

Get information about the cluster.

```
docker exec -it redpanda-0 rpk cluster info
```

💡 Create a new topic
================

Create a new topic called `chat-room`

```
docker exec -it redpanda-0 rpk topic create chat-room
```

You should see:

```
TOPIC       STATUS
chat-room  OK
```

💡 Produce a new topic message
================

Produce a message to the topic:

```
docker exec -it redpanda-0 rpk topic produce chat-room
```

Enter a message, then press Enter:

```
Pandas are fabulous!
```

Example output:

```
Produced to partition 0 at offset 0 with timestamp 1663282629789.
```

Press `Ctrl+C` to finish producing messages to the topic.

💡 Consume a new topic message
================

Consume one message from the topic:

```
docker exec -it redpanda-0 rpk topic consume chat-room --num 1
```

Your message is displayed along with its metadata,:

```
{
  "topic": "chat-room",
  "value": "Pandas are fabulous!",
  "timestamp": 1663282629789,
  "partition": 0,
  "offset": 0
}
```

🏁 Finish
=========

To complete the
challenge, press **Check**."
