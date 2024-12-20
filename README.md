# Dockerfile Port Conflict
This repository demonstrates a common Dockerfile error where the specified port in the `CMD` instruction conflicts with an existing process on the host machine.  The application fails to start because it cannot bind to the specified port.

## Problem
The original `Dockerfile` uses port 8000, which may already be in use.  This results in the container failing to start. 

## Solution
The solution involves either changing the port to an unused one or specifying a different port mapping between the container and the host using the `-p` flag with the `docker run` command. This example demonstrates the second approach.