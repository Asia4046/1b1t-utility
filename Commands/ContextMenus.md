# **ContextMenu Interactions**
## **Default Format**
```javascript
module.exports = {
    name: "cmdname",
    type: "cmdtype", // Either USER or MESSAGE
    run: async(client, interaction) => {
        // Your Stuff
    }
}
```

## **Example**
```javascript
const { ApplicationCommandType } = require("discord.js")
module.exports = {
    name: "log-content",
    type: ApplicationCommandType.Message,
    run: async(client, interaction) => {
        const msgContent = interaction.channel.messages.cache.get(interaction.targetId ?? await interaction.channel.messages.fetch(interaction.targetId)
        console.log(msgContent)
    }
}
```