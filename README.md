# A lightweight web server written in C

Server is a multi-threaded web server that supports both static and dynamic contents. It has a one-thread-multiple-active-clients architecture implemented using threadpools and handles large number of concurrent requests.

Server is implemented with some goals in mind:
* Fast and responsive
* Ability to handle large number of concurrent requests
* Support Python frameworks well

## Compilation
```
make
```
or
```
gcc server.c -o server -pthread
```

## Usage
Put index.html (default homepage), other pages and resources under the same directory. Then run:
```
./server [port]
```
You will see requests coming in.

## Dynamic content
Put your CGI binary under client directory and access it using
```
http://[your domain/ip address]:[port]/client/[program]?[parameter1]&[parameter2]&[...]
```
For example, to run the adder client program that comes with Server, go to:
```
http://[your domain/ip address]:[port]/client/adder?1+2
```

## Contribute
Please consider contributing to our project and learn with us along the way!
