# SKARTA23-Bot
SKARTA23-Bot is a powerful and customizable whatsapp chatbot  designed for media, group and downloads management AND MORE
```js
const { default: makeWASocket} = require('@adiwajshing/baileys');

async function startBot() {
  const sock = makeWASocket();
  sock.ev.on('messages.upsert', async ({ messages}) => {
    const msg = messages[0];
    if (!msg.key.fromMe && msg.message?.conversation === 'hi') {
      await sock.sendMessage(msg.key.remoteJid, { text: 'Hello! I am Skarta23-bot 🤖'});
}
});
}

startBot();


