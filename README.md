# simWebServer
This is a class project for CS3516 at WPI. This project aims to implement a server and a client using socket programming. The server can be deployed and accessed via the client or any browser. The client can download any resources supported by HTTP via the networks.

## How to run
### Server
1. Open up a terminal
2. `cd` into `simpleWebServer`
3. type in terminal `python http_server <port number>`, where the port number is specified by you (for instance, port 7893)
4. then if the terminal prints out `Socket successfully created` and `socket binded to port <port number>` it means he server has spun up

Example command to run the server:

`python http_server 7890`

####Client
1. Open up a terminal
2. `cd` into `simpleWebServer`
3. type in terminal `python http_client <optional flag> <url> <port number>`, where
    * the optional flag can be `--ttl`, which displaces the round trip time between the server and the client for the duration of the communication.
    * the url is the resource (currently only support html) that you want to download. For instance, http://hibou.cs.wpi.edu/~kven/courses/CS3516-B18/home.html
    * the port number is specified by you. For instance, port 7893.
4. the client will then download the html file and print out the whole file in the terminal.

Example command to run the client:

`python http_client localhost/TMDG.html 7890`

*note there are alternative ways to run this program, this is only one of the ways.*

## Default settings
* server is binded to localhost (127.0.0.1) with a port specified by the user.
* client is set to time out if the connection is hanged for more than 2 seconds.
* client is set to terminate if the client receives consecutive 10 blank responses.
