As of July 2014 [Heroku began supporting WebSockets](https://blog.heroku.com/websockets_now_ga) so the instructions below are no longer required. See [this Heroku article](https://devcenter.heroku.com/articles/node-websockets) for more information.

***

[Heroku](http://heroku.com) and [Socket.IO](https://github.com/LearnBoost/socket.io) do not play well out of the box with each other.  
To fix this, Socket.IO must have its transport set to **XHR-polling** with a **10 second interval**:

    io.set('transports', ['xhr-polling']);
    io.set('polling duration', 10);

See this [Heroku article](https://devcenter.heroku.com/articles/using-socket-io-with-node-js-on-heroku/) for more information.