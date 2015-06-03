# Data-Offloading-Using-EdgeServer

Mobile data offloading is term that is mostly used with cellular network. However, under a Wi-Fi network we can still use the concept of mobile data offloading. For example, a user wants to download an entire website for offline browsing. He can do this by writing a code to download the entire site from the server. However, if the user is using a slower device or a cellular phone then downloading an entire website may consume considerable amount of energy, CPU processing, memory and time. An alternate solution to this problem is to use a proxy server to do the downloading. We can assume that the server is located in a faster device, with a faster internet connection and the user client and the proxy server are under the same Wi-Fi LAN connection. The LAN connection will make the data transfer between the proxy server and user client faster. The client is also free from doing any processing regarding establishing connections to the server to request for the webpages. Under this setting, the user client only needs to send out the URL of the website to be downloaded to the proxy server. The proxy server will download the initial page and then parse that page for the links of local pages in the server. If it finds any, it will download those pages too. After obtaining all these pages, the proxy server can direct the pages to the user client.

The proxy server should be multithreaded. It should also keep a cache so that if there are multiple requests for one URL from several client users, it does not have to download the entire website for each request. The lifetime of the cache can be defined in the code.

As an output of the project you will do a performance comparison between the website
downloading with and without the proxy server. The performance metrics are CPU performance and end to- end delay for website downloading on the client side. To download the website you may use functions/method defined in a specific programming language (the language you will use to develop the program) but cannot use a third party function/method/program (e.g. wget).

Program Requirements:

Your program should –
1) Download entire website for a given URL (all the local pages only) on the client and the proxy server
2) Handle communication between client and proxy servers
3) Do a performance comparison between clients’s accessing web server by direct connection and using the Edge Server. The metrics are end-to-end delay and hardware resource consumption (CPU processing, memory usage, and/or energy consumption).
