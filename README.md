# websocket

parse socket buffer, add event emitter and cookie id

## download & install
    // in package.json
    "dependencies": {
      "node-websocket": ">=0.0.1"
    }
    $ npm install

## config & run

    // in your nodeserver file
    var ws = require('node-websocket').init;
    // bind events
    ws.on('connection', function(socketId) {});
    ws.on('join', function(data, socketId) {
      //send message
      ws.send('yes! it will send to frontend');
    });
    // you need start server in the end
    ws.start(8000);

## emit in frondend
    // you need creat socket object first
    socket.send(JSON.stringify({
      event: 'join',
      data: {
        room: room
      }
    }));

## all events & methods
* 'connection' event, emit when connect success
* Socket.prototype.on(eventName, callback);
* Socket.prototype.emit(eventName, data, socketId);
* Socket.prototype.send(data);
* Socket.prototype.start(port);

## bug && suggestion?
[Tell Me Please~](https://github.com/youngerheart/websocket/issues)
