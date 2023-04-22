# **Modal Forms**
## **Default Format**
```javascript
module.exports = {
    name: "cmdname",
    run: async(client, interaction) => {
        //stuff
    }
}
```

## **Example** // For creating the Modal cmd
```javascript
const { ApplicationCommandType, ActionRowBuilder, ModalBuilder, TextInputBuilder, TextInputStyle } = require("discord.js")
module.exports = {
    name: "modal",
    type: ApplicationCommandType.ChatInput,
    description: "Test Modal.",
    run: async(client, interaction) => {
        const modal = new ModalBuilder()
			.setCustomId('BasicInfoModal')
			.setTitle('My Modal');

		const favoriteColorInput = new TextInputBuilder()
			.setCustomId('favoriteColorInput')
			.setLabel("What's your favorite color?")
			.setStyle(TextInputStyle.Short);

		const hobbiesInput = new TextInputBuilder()
			.setCustomId('hobbiesInput')
			.setLabel("What's some of your favorite hobbies?")
			.setStyle(TextInputStyle.Paragraph);

		const firstActionRow = new ActionRowBuilder().addComponents(favoriteColorInput);
		const secondActionRow = new ActionRowBuilder().addComponents(hobbiesInput);

		// Add inputs to the modal
		modal.addComponents(firstActionRow, secondActionRow);

		// Show the modal to the user
		await interaction.showModal(modal);
    }
}
```

## **BasicInfoModal.js** // This file will contain your modal code.
```javascript
module.exports = {
    name: "BasicInfoModal",
    run: async(client, interaction) => {
        interaction.reply({
            content: "This is a correctly functioning modal."
        })
    }
}
```