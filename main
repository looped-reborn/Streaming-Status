require('dotenv').config();
const express = require('express');
const app = express();
app.get('/', (req, res) => {
    res.send('Self Bot Rich Presence working');
});
app.listen(process.env.PORT, () => {
    console.log('Self Bot Rich Presence working on port ' + process.env.PORT);
});

const Discord = require('discord.js-selfbot-v13');
const client = new Discord.Client({
    checkUpdate: false
});

client.on('ready', async () => {

    const rpc = new Discord.RichPresence()
        .setApplicationId('1106284259754377278')
        .setType('STREAMING')
        .setURL(`https://www.youtube.com/watch?v=EuXDc3P6mJU`)
        .setDetails(`dead`)
        .setName(`dead`)
        .setState(`souls`)
        .setParty({
            max: 999,
            current: 666,
            id: Discord.getUUID(),
        })
        .setAssetsLargeImage(`mp:attachments/1071183510255181974/1106581312145465374/hq720.jpg`)
        .setAssetsLargeText(`looped#1173`)
        .setAssetsSmallImage(`mp:attachments/1071183510255181974/1106582625755340980/m.jpg`)
        .setAssetsSmallText(`looped#1173`)
        .addButton(`looped.lol`, `http://looped.lol/`)
        .addButton(`looped.world`, `http://looped.world`);
    client.user.setActivity(rpc.toJSON());

    console.log(`${client.user.tag} is ready!`);
});

//Account Token
client.login(process.env.TOKEN);
