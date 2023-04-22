# **Non Client Events**
{% hint style="info" %}
**Note:** In the async function `run()` you can always call `client` after you call your required arguments for the event to access them.
{% endhint %}

## **Format**
```javascript
module.exports = {
    isCustom: true,
    run: async(<args>) => {
        //Code
    }
}
```

## **Example Usage**
```javascript
const Bababooey = require("something")
module.exports = {
    isCustom: true,
    run: async(client) => {
        Bababooey.on("yes", (e, E) => {
            //My code
        })
    }
}
```