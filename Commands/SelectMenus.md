# **SelectMenu Interactions**
## **Default Format**
```javascript
module.exports = {
    name: "name", // selectMenu's Custom ID or one of the options values.
    run: async(client, interaction) => {
        //Stuff
    }
}
```

## **Example**
### **SelectMenu Code**
```javascript
const { ActionRowBuilder, SelectMenuBuilder } = require("discord.js")
 const ActionRow = new ActionRowBuilder().addComponents(
            new SelectMenuBuilder()
            .setCustomId("SelectMenuExample")
            .setPlaceholder("Free Cookies!")
            .addOptions(
                [
                    {
                        label: "Click for cookies!",
                        description: "Freeee!",
                        value: "CookieBox"
                    }
                ]
            )
        )
```

### **bababooey.js**
```javascript
module.exports = {
    name: "CookieBox",
    run: async(client, interaction) => {
        interaction.reply({
            content: "Bababooey indeed"
        })
    }
}
```
