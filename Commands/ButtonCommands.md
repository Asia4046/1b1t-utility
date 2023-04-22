# **Button Interaction**

## **Default Format**
```javascript
module.exports = {
    name: "buttonName",
    run: async(client, interaction) => {
        // Do your dumb stuff.
    }
}
```
## **Example**
### **Button Code**
```javascript
const { ButtonBuilder, ActionRowBuilder } = require("discord.js")
 const row = new ActionRowBuilder()
            .addComponents(
                new ButtonBuilder()
                .setCustomId('deleteButton')
                .setLabel('Delete Output')
                .setStyle('Danger'),
            );
```

### **deleteButton.js**
```javascript
module.exports = {
    name: "deleteButton",
    ownerOnly: true,
    run: async(client, interaction) => {
        interaction.message.delete()
    }
}
```