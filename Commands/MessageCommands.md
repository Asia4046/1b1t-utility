# **Message / Normal Commands**
## **Default Format**
```javascript
module.exports = {
    name: "cmdname",
    run: async(client, message, args) => {
        //Do stuff
    }
}
```

## **Example**
```javascript
module.exports = {
    name: "ping",
    run: async(client, message, args) => {
        message.channel.send({
            content: `My ping is ${client.ws.ping}ms.`
        })
    }
}
```