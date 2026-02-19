
# What is Spring framework

Spring framework is lightweight java framework use to build enterprise level application.

## Core concept of Spring 

1. Dependency Injection (DI)
2. Inversion of Control (IOC)
3. Transaction Management(MVC)
4. Security
5. Microservices Development (via spring boot)

# 1. Dependency Injection

### Lets assume with real life example:

You are building a House.

House needs Electricity.
### Wrong Way

House builds its own power plant.

That makes no sense.
### Correct Way

Electricity is supplied from outside.

House depends on Electricity.  
But House does NOT create electricity.

That is Dependency Injection concept.

# Now Translate to Programming

A class often needs another class to work.

Example:

- Car needs Engine
- Service needs Repository
- Controller needs Service

The needed class is called:

 Dependency