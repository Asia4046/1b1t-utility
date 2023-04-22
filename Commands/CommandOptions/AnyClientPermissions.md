# **AnyClientPermissions**
## **About**
* When using this options, If the client (bot) has any one of the permissions in the array then it will continue else it will stop and send error message by default.

{% hint style="info" %}
**Note:** Make sure you put the permissions name correctly as they are case sensitive. For example: `ADMINISTRATOR` will not work instead use `Administrator`. You can find all the permissions correct names at [here](../../FAQ.md)
{% endhint %}
## **Usage**
```js
anyClientPermissions: ["Perm1", "Perm2"]
returnAnyClientPermissionsError: true / false // Default: true [ OPTIONAL ]
```
## **Example**
```js
anyClientPermissions: ["Administrator", "ManageEvents"]
```