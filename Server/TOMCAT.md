Why the spring boot application has not stop once the process completed like core Java. 
# Daemon vs non-daemon threads

Java has two broad categories:

```
Threads
 |
 +-- Non-daemon
 |
 +-- Daemon
```
### Non-daemon thread

Keeps JVM alive.

### Daemon thread

Doesn't prevent JVM shutdown.