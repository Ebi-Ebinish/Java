
# What is Spring framework

Spring framework is lightweight java framework use to build enterprise level application.

## Core concept of Spring 

1. Inversion of Control (IOC)
2. Dependency Injection(DI)
3. Transaction Management(MVC)
4. Security
5. Microservices Development (via spring boot)

Why the IOC and DI have exists means make the developers to focus on the business logic only and the other thinks spring will take care for that only these thinks are exists.

why the object creation is not done by us means we have to manage the creation of the object and the destroying all the thinks we have to do that's the spring or spring boot told hey developers you just focus on the main logic non other thinks I will manage.

# 1. Inversion of Control

In normally we have object creation control here we are giving that control to some one else.

Inversion of control it just a principle, Instead of you creating an Object your giving the control to Spring or some one else.

We need some technic to do IOC that's where the Dependency Injection comes there.

The Dependency injection is the actual implementation of Inversion of control
# 2. Dependency Injection

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

