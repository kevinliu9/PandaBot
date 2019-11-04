const Discord = require('discord.js');
const bot = new Discord.Client();
const PREFIX = 'mp!'
const stdin = process.openStdin();
const discord = require('discord.js');
var c = 10;
const quotes = ["barney is a dinsoaur from our imganatoin and wen hes tall hes waht we cal a dnisourar snsetaoin",
    "did you know that dolphins get high off pufferfish toxins",
    "you know carrots are amazing because you can shove em up your nose and wiggle em back and forth",
    "i love you red solo cup :D i lift you up :D let\'s have a partyyyy",
    "i like taping a kebab skewer to the front of my car and going 50 through a school zone to try and make a kebab",
    "Arima Kousei-kun... Kimi ga suki desu! Suki desu! Suki desu!",
    "you guys uh ever... freaking... rubbed a blob of play doh against a cheese grater?",
    "the huacaya is the most common type of alpaca. it outnumbers the Suri 9 to 1 in population and is most commonly found in argentina, bolivia, chile, and peru",
    "he\'s done it! he has done it! he has done it! seventy points! seventy points!",
    "no, rose, they are not breathing, and they have no arms or legs."
];
const swearwords = ["fuck", "shit", "bitch", "nigger", "nigga", "nig", "chink", "cunt", "dick", "pussy", "hoe"];
var quotes1 = [...quotes];

const token = 'NTk3ODA4OTY1MTAyOTkzNDcx.XSNfHw._XchC4fa6I0BLu_rBnrABcZxDgo';

bot.on('ready', () => {
    console.log('This bot is online!');
})
bot.on('guildMemberAdd', member => {
    const channel = member.guild.channels.find('name', 'bot-fun');
    if (!channel) { return; }
    channel.send(`Welcome to our server ${member} `);
})
bot.on('guildMemberRemove', member => {
    const channel = member.guild.channels.find('name', 'bot-fun');
    if (!channel) { return; }
    channel.send(`${member} left server :frowning:`);
})
stdin.addListener('data', (data) => {
    const channel = bot.channels.find('name', 'bot-fun');
    channel.send(data.toString());
});
bot.on('message', message => {

    if (message.content === ('no u') || message.content === ('no you')) {
        message.channel.sendMessage('no us all');
        message.react("599793901334953984");//emoji('599793901334953984'));
    }
    if (message.content === ('no me')) {
        message.channel.sendMessage('no us all');
        message.react("592161824934199317");//emoji('599793901334953984'));
    }
	/*if (bot.users.id == '363672636452110336') {
	message.channel.sendMessage('no us all');
	message.react("592161824934199317");//emoji('599793901334953984'));
	//message.react("599793901334953984");
	}
	/*if (message.channel.type == 'dm') {
        message.reply("You are DMing me now!");
    }*/
    if (message.content.includes('abcde')) {
        bot.users.get("552268717430407182").send("feed me inferior human");
    }
    for (var a = 0; a < swearwords.length; a++) {
        if (message.content.includes(swearwords[a])) {
            message.delete(1);
            message.channel.sendMessage('Stop cursing.');
        }
    }
    const words = message.content.split(' ');
    for (var b = 0; b < words.length; b++) {
        if (words[b] === 'meaty' || words[b] === 'panda' || words[b] === 'pandy') {
            var a = Math.floor(Math.random() * c + 0);
            message.channel.sendMessage(quotes1[a]);
            quotes1.splice(a, 1);
            c--;
            if (quotes1.length < 1) { quotes1 = [...quotes]; c = 10; }

        }
    }

	/*if (message.content === '!react-custom') {
	const emoji = bot.emojis.get('598307634554339358');
	message.react(`${emoji} `);*/


    let args = message.content.substring(PREFIX.length).split(" ");

    switch (args[0]) {
        case 'ping':
            //message.reply('pong!'); //pings you
            message.channel.sendMessage('pong!'); // doesn't ping you
            break;
        case 'clear':
            message.channel.bulkDelete(args[1]);
            break;
        case 'babypandas':
            var a = Math.floor(Math.random() * 5) + 1;
            if (a == 1)
                message.channel.send(/*"My Bot's message",*/ { files: ["https://s.abcnews.com/images/Lifestyle/gty_baby_pandas_02_jc_160930_4x3_992.jpg"] });
            else if (a == 2)
                message.channel.send(/*"My Bot's message",*/ { files: ["https://img.jakpost.net/c/2017/12/19/2017_12_19_37559_1513678721._large.jpg"] });

            else if (a == 3)
                message.channel.send(/*"My Bot's message",*/ { files: ["https://i.etsystatic.com/11931562/r/il/f3b271/1162163683/il_794xN.1162163683_jztr.jpg"] });
            else if (a == 4)
                message.channel.send(/*"My Bot's message",*/ { files: ["https://i.pinimg.com/originals/9b/13/9d/9b139d01794a55a6d12a3558d3fcd800.jpg"] });

            else if (a == 5)
                message.channel.send(/*"My Bot's message",*/ { files: ["https://media.npr.org/assets/img/2011/09/27/506128252_8907911_custom-f8aa64a0b75a6456cc652b4c037aa64470973709-s1500-c85.jpg"] });

            //else if(a == 6)
            //	message.channel.send(/*"My Bot's message",*/ {files: ["https://encrypted-tbn0.gstatic.com/images?q=tbn:ANd9GcS6AZk2-uKe7VAVkhPUMeaeIj4ybC8guOPW7XwsXr-6m8_5ORGz0w"]});

            //else if(a == 7)
            //message.channel.send(/*"My Bot's message",*/ {files: ["https://encrypted-tbn0.gstatic.com/images?q=tbn:ANd9GcTt1VMXyKsIQdyiId_Hi_lNPbwhPkfdEYxHYfnswcvjAUIhjxeKnw"]});
            //else if(a == 8)
            //message.channel.send(/*"My Bot's message",*/ {files: ["https://encrypted-tbn0.gstatic.com/images?q=tbn:ANd9GcQlTw8Bfj8ujLzXPaB3obYvcOZQbf0BSdY7XA2gtXO79Ju1k3BHpg"]});

            //else if(a == 9)
            //message.channel.send(/*"My Bot's message",*/ {files: ["https://encrypted-tbn0.gstatic.com/images?q=tbn:ANd9GcS09FY_hej6KXoLhRfg1eJIUeAPm3SppULNO1j2OzRE_lrZiT9O"]});
            //else if(a == 10)
            //message.channel.send(/*"My Bot's message",*/ {files: ["https://encrypted-tbn0.gstatic.com/images?q=tbn:ANd9GcTTa8yFz7l3-bz59g1ZphC61KQN1-EXpWNfixEAxcJSJmVkpgsVMA"]});
            /*async def on_message(self, message):
                if message.content.startswith('hi'):
                    await self.send_message(message.channel, 'no');*/
            break;
        case 'meatypanda':
            message.channel.sendMessage('<@!363672636452110336>');
            break;
        case 'sadcat':
            const ayy = bot.emojis.find(emoji => emoji.name === "sadcat");
            var catMessage = '';
            for (var a = 0; a < 20; a++) {
                catMessage += `${ayy} `;
            }
            message.channel.sendMessage(catMessage);
            break;
        case 'help':
            var resultMessage = '```Thank you so much for having me! <3 \n\nmp!babypandas is for random panda pictures because why not \nmp!sadcat spams a bunch of sadcats \nmp!meatypanda pings me (plz do not abuse) \nI guess that is it? Dang I needa start adding more o: \nLove you all! :D ```';
            message.channel.sendMessage(resultMessage);
            break;
        case 'kick':
            if (!args[1]) { message.channel.sendMessage('Please specify a person!'); break; }
            const user = message.mentions.users.first();

            if (user) {
                const member = message.guild.member(user);
                if (member) {
                    member.kick("Talk to Meaty why you were kicked.").then(() => {
                        message.reply('Successfully kicked ' + user.tag);
                    }).catch(err => {
                        message.reply('Unable to kick member');
                    });
                } else {
                    message.reply('Not in the guild!');
                }
            } else {
                message.reply('Not in the guild!');
            }
            break;
        case 'ban':
            if (!args[1]) { message.channel.sendMessage('Please specify a person!'); break; }
            const theUser = message.mentions.users.first();

            if (theUser) {
                const theMember = message.guild.member(theUser);
                if (theMember) {
                    theMember.ban("Talk to Meaty why you were banned.").then(() => {
                        message.reply('Successfully banned ' + theUser.tag);
                    }).catch(err => {
                        message.reply('Unable to ban member');
                    });
                } else {
                    message.reply('Not in the guild!');
                }
            } else {
                message.reply('Not in the guild!');
            }
            break;
        case 'addRole':
            if (!args[1]) { message.channel.sendMessage('Please specify a person!'); break; }
            if (!args[2]) { message.channel.sendMessage('Please specify a role!'); break; }
            else {
                var roleName = '';
                for (var a = 2; a <= args.length; a++) {
                    if (!args[a]) { roleName = roleName; }
                    else {
                        roleName += args[a] += ' ';
                    }
                }
                var role = message.guild.roles.find('name', roleName.toString());
                var member = message.mentions.members.first();
                member.addRole(role);
            }





    };



})

bot.login(token);