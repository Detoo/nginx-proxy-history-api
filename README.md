# Test nginx configuration for HTML5 History API

The HTML5 History API [enables manipulating browser history via scripts](http://diveintohtml5.info/history.html). 
Single-Page Application can utilize such API to allow routing/navigation in a way similar to the conventional multi-page 
website does but requires no page reload; however, when the user hits the refresh button, there is no way for 
the web server to draw the boundary between front-end and back-end routing. The Single-Page Application would not 
reload as expected.

This project demonstrates a solution by configuring nginx to serve all static assets while passing through all other 
routes to the application root(index.html) and let it handle the remainder route in the front-end. In the meantime, 
we can still configure nginx to reverse-proxy API calls.


# Usage

```
docker-compose up
curl http://localhost
curl http://localhost/api/hello
curl http://localhost/test.txt
curl http://localhost/frontend/route/example
```
