## What is Apache Kafka?

**Kafka is a system that lets applications send messages to each other reliably and at high speed.**

Think of it as a **big message pipeline** between different services.

Instead of one service calling another directly, they send messages through Kafka.

# 🔹 Very Simple Example (Food Delivery App)

Imagine you have a food delivery app with 3 services:

- 🛒 Order Service
- 💳 Payment Service
- 📧 Notification Service
### Without Kafka

Order Service calls:

- Payment Service
- Then Notification Service

If Payment Service is down → everything fails ❌