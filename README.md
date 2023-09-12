const { Client, GatewayIntentBits } = require('discord.js')
const { Guilds, GuildMessages, MessageContent } = GatewayIntentBits
const client = new Client({ intents: [Guilds, GuildMessages, MessageContent] })
client.login('MTE0NzMxNTYwNDY5MzQ1NDg4OA.GVugBp.DF4oEC2S1g5kc1aCvMRr5Qji4GST1x-qXlmxes')

client.once('ready', () => console.log(''))
client.on('messageCreate', message => {
  if (message.content === 'ping')
    message.reply('pong')
})

require('./server')()
