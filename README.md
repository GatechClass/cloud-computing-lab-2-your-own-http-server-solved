# cloud-computing-lab-2-your-own-http-server-solved
**TO GET THIS SOLUTION VISIT:** [Cloud Computing Lab 2-Your Own HTTP Server Solved](https://mantutor.com/product/cloud-computing-lab2-your-own-http-server-solved/)


---

**For Custom/Order Solutions:** **Email:** mantutorcodes@gmail.com  

*We deliver quick, professional, and affordable assignment help.*

---

<h2>Description</h2>



<div class="kk-star-ratings kksr-auto kksr-align-center kksr-valign-top" data-payload="{&quot;align&quot;:&quot;center&quot;,&quot;id&quot;:&quot;113891&quot;,&quot;slug&quot;:&quot;default&quot;,&quot;valign&quot;:&quot;top&quot;,&quot;ignore&quot;:&quot;&quot;,&quot;reference&quot;:&quot;auto&quot;,&quot;class&quot;:&quot;&quot;,&quot;count&quot;:&quot;1&quot;,&quot;legendonly&quot;:&quot;&quot;,&quot;readonly&quot;:&quot;&quot;,&quot;score&quot;:&quot;5&quot;,&quot;starsonly&quot;:&quot;&quot;,&quot;best&quot;:&quot;5&quot;,&quot;gap&quot;:&quot;4&quot;,&quot;greet&quot;:&quot;Rate this product&quot;,&quot;legend&quot;:&quot;5\/5 - (1 vote)&quot;,&quot;size&quot;:&quot;24&quot;,&quot;title&quot;:&quot;Cloud Computing  Lab 2-Your Own HTTP Server Solved&quot;,&quot;width&quot;:&quot;138&quot;,&quot;_legend&quot;:&quot;{score}\/{best} - ({count} {votes})&quot;,&quot;font_factor&quot;:&quot;1.25&quot;}">

<div class="kksr-stars">

<div class="kksr-stars-inactive">
            <div class="kksr-star" data-star="1" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" data-star="2" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" data-star="3" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" data-star="4" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" data-star="5" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
    </div>

<div class="kksr-stars-active" style="width: 138px;">
            <div class="kksr-star" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
    </div>
</div>


<div class="kksr-legend" style="font-size: 19.2px;">
            5/5 - (1 vote)    </div>
    </div>
All materials of lab2 are in folder Lab2/.

1. Overview

Implement an HTTP server based on HTTP/1.1 from scratch by your own, using network programming knowledges learned from our class.

Also, try to use high concurrency programming skills learned from the class to guarantee the web server’s performance.

Our Goals:

Practice basic network programming skills, such as using socket API, parsing packets; Get familiar with robust and high-performance concurrent programming.

2. Backround

Please check background.md first to learn some basics about HTTP, HTTP messages , HTTP proxy, JSON &amp; curl.

3. Your Lab Task

Implement your own HTTP Server

In this Lab, we won’t provide any basic code. You should implement an HTTP server based on HTTP/1.1, from scratch which satisfies the following requirements:

HTTP Server Outline

From a network standpoint, your HTTP server should implement the following:

1. Create a listening socket and bind it to a port;

2. Wait a client to connect to the port;

3. Accept the client and obtain a new connection socket;

4. Read in and parse the HTTP request;

5. Start delivering services (some are optional):

6. Handle HTTP GET/POST requests and return responses.

7. Proxy the request to another HTTP server.

The server will be in either non-proxy mode or proxy mode (we have introduced the proxy in background section 2.3). It does not do both things at the same time.

For better testing and scoring, we have made some functional requirements for your submitted works.

ATTENTION: Lab 2 is a pre-lab of Lab 4. If you plan to complete Lab 4, please complete the advanced version of Lab 2.

3.1 Handle HTTP request &amp; send HTTP response

In this Lab, you just need to implement the GET method and the POST method in your HTTP server.

For any other methods, your server should send a response with 501 status code (see 2.2). That is to say, if your HTTP server receive an HTTP request but the request method is neither GET nor POST, the HTTP server just need to return a 501 Not Implemented error message (a response message with Response line having status code to be 501, see 2.2).

See examples in section 3.7.

3.1.1 Handle HTTP GET request

The HTTP server should be able to handle HTTP GET requests for specific resources, e.g., web service data &amp; static files.

For a GET request, the server needs to check whether the path of request corresponds to a web service or an existed static file.

What you need to do:

basic version:

A search service: use a specific url to get some data from the server that does not come from a file stored on the file system. The url don’t have query string, e.g. http://localhost:8080/api/check; Send response with plain text content.

Static files access: use a specific url to access a text file stored on the file system.

Clients only request *.html;

Send response with the full content of html file.

If the path is invalid or the static file does not exist

Send response with the full content of 404 Not Found page.

advanced version:

A search service: use a specific url to get some data from the server that does not come from a file stored on the file system.

Or if invalid, send response with json type content, including error messages;

Static files access: use a specific url to access a text file stored on the file system.

Send Response with the correct Content-Type &amp; the full content of the file.

If the path is invalid or the static file does not exist

Send response with the full content of 404 Not Found page.

You don’t need to implement to transmit base64 encoded binary files, such as image files like *.png.

3.1.2 Handle HTTP POST request

The HTTP server should be able to handle HTTP POST requests.

For a POST request, the server needs to check whether the path of request corresponds to a web service.

What you need to do:

basic version:

A upload service: use a specific url to upload some data to the server

The content type is application/x-www-form-urlencoded;

The payload contains key-value pairs, keys are id &amp; name;

If the payload is valid, send response with 200 OK, Content-Type: text/plain &amp; data;

Or if the payload invalid, send response with send response with 404 Not Found, Content-Type: text/plain &amp; error messages;

If the path is invalid

Send response with the full content of 404 Not Found page.

advanced version:

A upload service: use a specific url to upload some data from the server that does not come from a file stored on the file system.

The content type is application/x-www-form-urlencoded, application/json;

The payload contains key-value pairs, keys are id &amp; name;

If the payload is valid, send response with 200 OK, Content-Type: application/json &amp; data;

Or if the payload invalid, send response with send response with 404 Not Found, Content-Type: application/json &amp; error messages;

If the path is invalid

Send response with the full content of 404 Not Found page.

If you are not familiered with application/x-www-form-urlencoded, check MDN docs.

3.1.3 Other request

Just return 501 Not Implemented page for other request method (e.g. DELETE, PUT, etc.).

3.2 Implement a proxy server (optional for advanced version)

Enable your server to proxy HTTP requests to another HTTP server and forward the responses to the clients.

1. You should use the value of the –proxy command line argument, which contains the address and port number of the upstream HTTP server.

2. Your proxy server should wait for new data on both sockets (the HTTP client file descriptor, and the upstream HTTP server file descriptor). When data arrives, you should immediately read it to a buffer and then write it to the other socket. You are essentially maintaining 2-way communication between the HTTP client and the upstream HTTP server. Note that your proxy must support multiple requests/responses.

3. If either of the sockets closes, communication cannot continue, so you should close the other socket and exit the child process.

Hints: 1) This is more tricky than writing to a file or reading from stdin, since you do not know which side of the 2-way stream will write data first, or whether they will write more data after receiving a response. 2) You should again use threads for this task. For example, consider using two threads to facilitate the two-way communication, one from A to B and the other from B to A.

It is not our task to implement protocols other than HTTP.

They often involve encryption algorithms and are difficult to implement directly using socket api.

However, if you are interested in protocols such as HTTPS, you can try to use other libraries, e.g. openssl.

3.3 Use multi-thread to increase concurrency

Your HTTP server should use multiple threads to handle as many concurrent clients’ requests as possible. You have at least the following three options to architect your multi-thread server:

Combined. Combine above two styles together. For example, you can use thread pool to receive request and send response, and use ondemand threads to fetch large page files.

Feel free to choose any one from the above three, or use other multi-thread architecture that you think is cool.

3.4 Support HTTP pipelining

In the basic version, you have only one request per TCP connection going on at the same time. The client waits for response, and when it gets response, perhaps reuses the TCP connection for a new request (or use a new TCP connection). This is also what normal HTTP server supports.

In the advanced version, multiple http requests can be fired concurrently on one TCP connection. This is also called HTTP pipelining which is supported by many real browsers and servers (such as Chrome). Note that HTTP requests that come from the same TCP connection should be responded in the same order. So take care the order problem when using complex multi-thread styles.

3.5 Specify arguments

Your program should enable long options to accept arguments and specify those arguments during start.

They are:

| arguments | descriptions | | — | — | | -i, –ip &lt;IP&gt; | Specify the server IP address. | | -p, –port &lt;PORT&gt; | Selects which port the HTTP server listens on for incoming connections. | | –proxy &lt;PROXY&gt; | Selects an “upstream” HTTP server to proxy. | | -t, –threads &lt;THREADS&gt; | Number of threads if you use multi-thread. |

The –proxy can have a schema before :// and a port number after a colon (e.g. http://www.example.com:80). If a port number is not specified, port 80 is the default for HTTP.

3.6 Run your HTTP Server

For advanced version:

Your program should be able to start at terminal. If your program is called http-server, just typing:

in the non-proxy mode:

./http-server –ip 127.0.0.1 –port 8888 –threads 8

It means that your HTTP server’s IP address is 127.0.0.1 and service port is 8888. The –number-thread indicates that there are 8 threads in the thread pool for handling multiple client request concurrently.

in the proxy mode:

./http-server –ip 127.0.0.1 –port 8888 –threads 8 –proxy http://www.example.com:80

It means that this is an HTTP proxy server. This proxy’s IP address is 127.0.0.1 and service port is 8888. And the proxy has a thread pool with 8 threads. The –proxy indicates that the “upstream” HTTP server is http://www.example.com:80. So, if you send a request message to this proxy (i.e. 127.0.0.1:8888), it will forward this request message to the “upstream” HTTP server (i.e. http://www.example.com:80) and forward the response message to the client.

If you want to access this server from other host, maybe you should open the firewall corresponding to the port and bind the ip to 0.0.0.0.

When you run the command above, your HTTP server should run correctly.

3.7 Access Your HTTP Server

We assume that the ip the server bound is 127.0.0.1 and the port is 8080. If the proxy feature is used, the remote server is www.example.com.

For more efficient testing and scoring, we need you to implement some of the interfaces described below, and make sure that the content of the response is consistent with our expectations.

That’s why we provide some standard static files. You can check those files in ./static/ &amp; ./data/.

Please make sure your server supports accessing them, and do not modify their content or relative paths.

3.7.1 Using GET method

1) access static files For basic version:

| path | files in local fs | status code | content type | | — | — | — | — | | /, /index.html | /{static dir}/index.html | 200 | text/html | | /404.html |

/{static dir}/404.html | 404 | text/html | | /501.html | /{static dir}/501.html | 501 | text/html | | any other error paths | /{static dir}/404.html | 404 |text/html | E.g.:

“`shell user@linux:~/http-server$ curl -i -X GET http://localhost:8080/index.html HTTP/1.1 200 OK Content-Type: text/html Content-Length:

210

index.html

“`

For advanced version:

| path | files in local fs | status code | content type | | — | — | — | — | | /, /index.html | /{static dir}/index.html | 200 | text/html | | /404.html |

/{static dir}/404.html | 404 | text/html | | /501.html | /{static dir}/501.html | 501 | text/html | | [/*]/*.html | /{static dir}[/*]/*.html |

200 | text/html | | [/*]/*.js | /{static dir}[/*]/*.js | 200 | text/javascript | | [/*]/*.css | /{static dir}[/*]/*.css | 200 | text/css | | [/*]/*.json |

/{static dir}[/*]/*.json | 200 | application/json | | any other error paths | /{static dir}/404.html | 404 | text/html |

“` user@linux:~/http-server$ curl -i -X GET http://localhost:8080/data.json HTTP/1.1 200 OK Content-Type: application/json Content-Length:

93

[{“id”:1,”name”:”Foo”},{“id”:2,”name”:”Bar”},{“id”:3,”name”:”Foo Bar”},{“id”:4,”name”:”Foo”}] “`

For standardized testing, output JSON data in one line without unnecessary spaces. 2) access web services for getting data For basic version:

| path | get data | status code | content type | | — | — | — | — | | /api/check | strings in data.txt | 200 | text/plain | | any other error paths |

/{static files}/404.html | 404 | text/html | E.g.:

“`shell user@linux:~/http-server$ curl -i -X GET http://localhost:8080/api/check HTTP/1.1 200 OK Content-Type: text/plain Content-Length: 13 id=1&amp;name=Foo “`

For advanced version:

| path | get data | status code | content type | | — | — | — | — | | /api/list | all objects in data.json | 200 | application/json | | /api/search? [id=value1&amp;name=value2] | all objects that match

*.id == value1 &amp;&amp; *.name == value2

in /data/data.json | 200 | application/json | | /api/search?[id=value1&amp;name=value2] | if no object matches, return all objects in /data/not_found.json | 404 |application/json | | any other error paths | /{static files}/404.html | 404 | text/html |

The query string format is a regular expression: id=[0-9]+&amp;name=[a-zA-Z0-9]+.

If you do not want to parse json file, you could store the data in memory instead of reading file every time. E.g.:

“`shell user@linux:~/http-server$ curl -i -G -d ‘id=1&amp;name=Foo’

-X GET http://localhost:8080/api/search HTTP/1.1 200 OK Content-Type: application/json Content-Length: 23

[{“id”:1,”name”:”Foo”}] “`

For standardized testing, output JSON data in one line without unnecessary spaces.

3.7.2 Using POST method access web services for uploading data

All data you need to upload are two key/value pairs: id: {value1} &amp; name: {value2}.

For standardized testing, output in the order of id, name.

Your server should check the data. In default case, the server should echo the data from the client.

If the data format is error, e.g., id=1&amp;name, id=1 or id=1&amp;foo=a, send content error message.

For basic version:

The client should send requests with Content-Type: application/x-www-form-urlencoded.

The echo data format is a regular expression: id=[0-9]+&amp;name=[a-zA-Z0-9]+.

After handling, send response:

| path | content | status code | content type | | — | — | — | — | | /api/echo | echo the data received | 200 | application/x-www-form-urlencoded | |

/api/echo | if the data format is error, send strings in /data/error.txt | 404 | text/plain | | any other error paths | /{static files}/404.html | 404 | text/html | E.g.:

“`shell user@linux:~/http-server$ curl -i -d ‘id=1&amp;name=Foo’

-H ‘Content-Type: application/x-www-form-urlencoded’ -X POST http://localhost:8080/api/echo HTTP/1.1 200 OK ContentType: application/x-www-form-urlencoded Content-Length: 13 id=1&amp;name=Foo “`

For advanced version:

The client should send requests with Content-Type: * application/x-www-form-urlencoded, * application/json.

After handling, send response:

| path | content | status code | content type | | — | — | — | — | | /api/upload | echo the data received | 200 | application/json | | /api/upload | if the data format is error, send strings in /data/error.json | 404 | application/json | | any other error paths | /{static files}/404.html | 404 | text/html | E.g.:

“`shell user@linux:~/http-server$ curl -i -d ‘{“id”:1,”name”:”Foo”}’

-H ‘Content-Type: application/json’ -X POST http://localhost:8080/api/upload HTTP/1.1 200 OK Content-Type: application/json Content-Length: 21 {“id”:1,”name”:”Foo”} “`

For standardized testing, output JSON data in one line without unnecessary spaces.

3.7.3 Other method

The HTTP server will not handle HTTP requests except GET requests and POST requests.

If you send an HTTP request with DELETE (or PUT, HEAD, etc.) to delete the specified resource, your server should send /{static dir}/501.html:

3.8 Implementation requirements

Version

Basic version

Complete all the tasks of the basic version described in section 3.1.1~3.1.7 except 3.1.3 &amp; 3.1.4.

Advanced version

Complete all the tasks of the advanced version described in section 3.1.1~3.1.7 including 3.1.3 &amp; 3.1.4.

4. Tester

We provide some tools for testing.

You can check the repos of the tester.

Of course you can also use your own browser and other web tools like curl.

5. Lab submission

Please submit your lab program following the guidance in the Overall Lab Instructions (../README.md)

6. Grading standards

You can get 28 points if you can:

finish all the requirements of the basic version

You can get 30 points (full score) if you can:

finish all the requirements of the advanced version

If you missed some parts, you will get part of the points depending how much you finished.
