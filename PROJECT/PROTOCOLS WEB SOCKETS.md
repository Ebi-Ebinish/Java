### What is web sockets?
Web Socket is a protocol that allows two-way, real-time communication over one persistent (தொடர்ந்து) connection.

---
## How HTTP communication works?

### Step-by-step flow:
1. Browser sends HTTP request  
2. Server processes request  
3. Server sends HTTP response  
4. Connection closes  

### Visually:
	Client → Request → Server  
	Client ← Response ← Server  
	(Connection closed)

---
## VERY IMPORTANT POINT
After the response, the server forgets the client.  
There is no continuous connection.

---
## The fundamental limitation of HTTP

HTTP has a strict rule:  

Only the client can start communication  

The server:
- CANNOT send data on its own  
- MUST wait for a client request  

### This means:
1. Server has new data  
2. Client didn't ask yet  
3. Server must stay silent  

---
## Let’s fix it with polling:

### 1. Short Polling:
The client sends requests to the server at regular, short time intervals, whether or not data is available.
#### How polling works:

	Client → Request  
	Server → Response (immediate)  
	Connection closes

	(wait 1–5 seconds)

	Client → Request again

#### Problems with polling:
- Too many useless requests  
- High server load  
- Delayed updates  
- Waste of bandwidth  

---
### 2. Long Polling:
The client sends a request and the server keeps the connection open until data is available (or timeout occurs).

#### How it works:
	Client → Request  
	(Server waits…)  
	Server → Response (when data arrives)  
	Connection closes
	Client immediately sends a new request


#### Key characteristics:
- Client does NOT keep asking  
- Server waits  
- Fewer useless responses  
- Faster than short polling  
---
## What is Server-Sent Events (SSE)?
