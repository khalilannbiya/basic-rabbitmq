# Learning the Basics of RabbitMQ as a Message Broker

The purpose of this project is to understand the use of a message broker, and this time we are using RabbitMQ as the message broker. Remember, RabbitMQ is a message broker that is responsible for receiving and delivering messages. You can think of a message broker as a postal worker who can receive messages from senders and deliver them to recipients. The difference between RabbitMQ and a typical postal worker is that RabbitMQ doesn't accept paper as messages; instead, it receives data collections in the form of buffers known as messages. Here are some terms you need to understand when building a message broker using RabbitMQ: Producing: The activity of sending messages. The party or program sending messages is called a producer. Queue: A mailbox located on the RabbitMQ server that can hold many messages. Despite its capacity for many messages, a queue still has limits, especially when messages contain large buffers. Consuming: The activity of receiving messages. The party or program receiving messages is called a consumer. Consumers continuously monitor the queues on the RabbitMQ server while they are available or capable of receiving messages.

## Tech Stack
- **Server :** Nodejs, RabbitMQ

## Run Locally

Clone the project

```bash
  git clone https://github.com/khalilannbiya/basic-rabbitmq.git
```
Or Download ZIP

[Link](https://github.com/khalilannbiya/basic-rabbitmq/archive/refs/heads/main.zip)

Go to the project directory

```bash
  cd basic-rabbitmq
```

Make sure you have RabbitMQ installed locally. If you haven't already, you can install it from [Download RabbitMQ](https://www.rabbitmq.com/download.html). Choose the version that matches your operating system. In my case, I installed it using the Windows Installer.

If you haven't installed Erlang on your computer, you'll receive a warning. Please install Erlang from here: [Download Erlang](https://www.erlang.org/downloads) and make sure it matches the RabbitMQ version here: [Make sure](https://www.rabbitmq.com/which-erlang.html).

Try installing RabbitMQ again after successfully installing Erlang.

The installation process is complete! To ensure that the RabbitMQ server is running on your computer, you can check it through the RabbitMQ management page. However, to access it, we need to enable the rabbitmq_management plugin. To do this, in the Windows search, look for "RabbitMQ Command" and then enter the following command:

```bash
  rabbitmq-plugins.bat enable rabbitmq_management
```

Please visit the address http://localhost:15672 and enter the username and password with the value "guest".

Move to the "Queues" tab. On this queues page, you will see a list of active messages as well as those that have been sent to consumers.

Install node_modules

```bash
  pnpm i
```

To send a message, run 

```bash
  node producer.js
```

To consume or receive messages sent by the producer, run the command
```bash
  node consumer.js
```

## Documentation

- [Nodejs](https://nodejs.org/en)
- [Rabbit MQ](https://www.rabbitmq.com/)
- [Mengapa Message Broker](https://medium.com/@acep.abdurohman90/mengapa-menggunakan-message-broker-c17453cb225e)

## Feedback

If you have any feedback, please reach out to us at syeichkhalil@gmail.com
