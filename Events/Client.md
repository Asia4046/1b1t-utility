# **Client Events**
{% hint style="info" %}
**Note:** In the async function `run()` you can always call `client, container` after you call your required arguments for the event to access them.
{% endhint %}

## **Format**
```javascript
module.exports = {
    name: "eventName",
    runOnce: false, // Whether to run the event only once.
    run: async(<args>) => {
        //Code
    }
}
```

## **Example Usage**
```javascript
module.exports = {
    name: "messageUpdate",
    run: async(client, oldMessage, newMessage) => {
        //Your code
    }
}
```