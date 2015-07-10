# websocket

parse socket buffer, add event emitter and cookie id

## install

    npm install

## config & run

    // in your nodeserver file
    var ws = require('./websocket').init;
    // bind events
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

## all methods

* Socket.prototype.on(eventName, callback);
* Socket.prototype.emit(eventName, arg1, arg2, ...);
* Socket.prototype.send(data);
* Socket.prototype.start(port);

## bug && suggestion?
[Tell Me Please~](https://github.com/youngerheart/websocket/issues)
