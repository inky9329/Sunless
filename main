// Require discord.js package
const Discord = require("discord.js");
 
// Create a new client using the new keyword
const client = new Discord.Client();
 
// date format for the event date
const eventDate = "2020-01-13 18:00:00";
 
// placeholder formatting string
const format = "m/d/y H:M";
 
// variables for hours and minutes in milliseconds
const hourInMs = 3600000;
const minuteInMs = 60000;
 
// Display a message once the bot has started
client.on("ready", () => {
    console.log(`Logged in as ${client.user.tag}!`);
});
 
//Jokes command
 
client.on('message', async msg => {
    if (msg.content === "!joke")
        var jokeRoll = Math.floor((Math.random() * 10) + 1)
    if (jokeRoll === 1) {
        msg.reply("I went to the doctors recently\n He said: “Don’t eat anything fatty”\n I said: “What, like bacon and burgers?”\n He said, “No. fatty don’t eat anything. \n-u/MissDeeMeeNor");
    }
    if (jokeRoll === 2) {
        msg.reply("It should be more like - A woman is walking home with her 3 daughters. The eldest daughter turns to her and asks, 'Mummy, how did I get my name?' 'Well sweetie, when we were bringing you home from the hospital, a rose petal landed on your head! So that's why we named you Rose.' The second daughter, now curious, asks the same question. 'Well darling, when we were bringing you home from the hospital, a lily petal landed on your head! So that's why we named you Lily.' The third girl asks 'HHGHGNGHGHNG?!?!?! DDDNBHGHBHNGHHH!!!'. 'Shhh, quiet now, Cinderblock.'\n-u/Marowak");
    }
    if (jokeRoll === 3) {
        msg.reply("I think the Rainforest Cafe takes the whole rainforest theme too far. This one time I was sitting there eating my chicken tenders and they bulldozed 40% of the restaurant.\n-u/adamMclfresh");
    }
    if (jokeRoll === 4) {
        msg.reply("Dad is listening to his daughter say her prayers before bedtime. She says - God bless mommy and god bless daddy and god bless grandma and... goodbye grandpa. He asks her - why did you say that? I don't know, I just felt like saying it. The next day, grandpa drops dead. Wow, thinks dad, that's an odd coincidence. A month later at bedtime, the daughter says - God bless mommy and daddy. And goodbye grandma. Sure enough, the next day grandma breathes her last earthly breath. The dad realizes this is more than a coincidence, but he is not sure what to do. He doesn't want to disturb his wife by telling her (Grandma and grandpa were her parents). Months go by and one night the man is listening to his daughter saying her prayers at bedtime - God bless mommy....she turns her head and looks straight at him - and goodbye daddy. What!? are you sure honey? She nods. The man's heart begins racing and he breaks out in a sweat. He is so upset, he can't sleep at all that night. The next day he goes off to work, but locks himself in his office. He takes the phone off the hook, cancels all his meetings and awaits the inevitable. He stays at work past 5 because he feels secure there. He watches the hours tick by. Finally it is midnight and, drenched in sweat, he realizes he has cheated death. He drives home drenched in sweat and with all his nerves frazzled. His wife is up and waiting for him - Where the hell were you today??! He replies - Don't shout, I've had an absolutely miserable day. His wife then says - You had a miserable day? I'm the one who had a miserable day! First, the milkman drops dead on the steps... \n-u/BloodAndBroccoli");
    }
    if (jokeRoll === 5) {
        msg.reply("Never tell a pun to a kleptomaniac. They're always taking things literally. \n-u/jackhackery");
    }
    if (jokeRoll === 6) {
        msg.reply("You’ve heard of Murphy’s law right? It says that anything that can go wrong will go wrong. But have you heard of Cole’s law? It’s thinly sliced cabbage.\n-u/ItsSam_JK");
    }
    if (jokeRoll === 7) {
        msg.reply("What do you get when you cross a joke with a rhetorical question?\n-u/kabobstr");
    }
    if (jokeRoll === 8) {
        msg.reply("I stand corrected, said the man in the orthopaedic shoes\n-u/VerbableNouns");
    }
    if (jokeRoll === 9) {
        msg.reply("A woman is sitting at her recently deceased husband’s funeral. A man leans in to her and asks, “Do you mind if I say a word?”. “No, go right ahead”, the woman replies. The man stands, clears his throat, says “Plethora”, and sits back down. “Thanks”, the woman says, “that means a lot”.\n-u/jimbojones230");
    }
    if (jokeRoll === 10) {
        msg.reply("Do you know the reason why the Sweedish navy has barcodes on their ships? So they can Scandanavian.\n-u/RacingNeilo");
    }
});
 
 
 
//!staffhelp Command
client.on('message', async msg => {
    //console log the object when writing a specific command
    if (msg.content === "!staffhelp") {
        client.channels.get("613871430416859154").reply("<@&597871142170263552>, user <@!" + msg.author.id + "> needs staff help in <#" + msg.channel.id + ">");
 
    }
 
 
});
//!serverinfo Command
client.on('message', async msg => {
    //Display some data about the current server
    if (msg.content === "!serverinfo") {
        console.log(msg.channel.TextChannel);
        console.log(msg.TextChannel);
        msg.reply("Channel name: <#" + msg.channel.id + "> \n " +
            "nsfw: " + msg.channel.nsfw + "\n " +
            "Members on server: " + msg.channel.guild.memberCount + "\n ");
    }
    //Only reply if the user writes in bot-testing channel
    else if (msg.content === "!nsfw") {
        //Not limited to msg.content
        if (msg.channel.nsfw) {
            msg.reply("This channel is 18+")
        }
        if (!msg.channel.nsfw) {
            msg.reply("This channel is not 18+")
        }
    }
    //Reply details about the author who sent the message
    else if (msg.content === "!authorinfo") {
        msg.reply("Author's name is: " + msg.author.username + "#" + msg.author.discriminator + "\n Is a bot? " + msg.author.bot);
    }
    //Calculate when the server was created using the joinTimeStamp milliseconds
    else if (msg.content === "!created") {
        //Require node datetime package
        var datetime = require('node-datetime');
 
        //Store the createdTimestamp MS value in a variable
        var past = msg.channel.guild.createdTimestamp;
 
        console.log(past);
 
        //Create a date with the MS value
        var pastDateTime = datetime.create(past);
 
        //Format the date, making it readable
        var formatted = pastDateTime.format('m/d/Y H:M:S');
 
        msg.reply("The server was created: " + formatted);
    }
    //More server info
    else if (msg.content === "!moreinfo") {
        //name, nsfw, id, region, afktimeout
        // console.log(msg.channel.guild);
        msg.reply("Server name is: " + msg.channel.guild.name + "\n Id is: " + msg.channel.guild.id +
            "\n AFK timeout is: " + msg.channel.guild.afktimeout + "s\n Server Region is: " + msg.channel.guild.region +
            "\n Channel written in nsfw status: " + msg.channel.nsfw);
    }
    //last message info (info about author and message)
    else if (msg.content === "!lastmessage") {
        msg.reply("Your last message sent was " + msg.channel.lastMessage.content + "\n Your name is " + msg.channel.lastMessage.author.username +
            "#" + msg.channel.lastMessage.author.discriminator + "\n Are you a bot? " + msg.channel.lastMessage.author.bot +
            "\n And message id is " + msg.channel.lastMessageID);
    }
 
    //Name and Discriminator of each member in the server and amount of members 
    else if (msg.content === "!membersinfo") {
        msg.channel.guild.members.forEach(function (mber) {
            if (mber.user.bot) {
                client.channels.get("613871430416859154").reply("Username: " + mber.user.username + "#" + mber.user.discriminator +
                    " This user is a bot.")
            } else if (!mber.user.bot) {
                client.channels.get("613871430416859154").reply("Username: " + mber.user.username + "#" + mber.user.discriminator +
                    " This user is NOT a bot.")
            }
        });
    }
});
 
// Check messages for a specific command
client.on("message", async msg => {
    // check for !commands
    if (msg.content === "!commands") {
        msg.reply("This bot's commands are: \n !.commands: Shows a list of commands for the bot! \n !.event: Shows the time until the next event! \n !.author: Shows info about the author of the bot\n !.staffhelp: Notifies staff of an issue. This pings all staff so please use it responsibly. \n !.serverinfo: Displays info about the server! \n !.nsfw: Checks if the channel is nsfw or not! \n !.authorinfo: Returns info on the author! \n !.created: Shows the date of server creation! \n !.moreinfo: Displays more info about the server! \n !.lastmessage: Returns info about the last message. \n !.membersinfo: This returns the tags of ALL server members and if they are a bot! \n !.mediumclue: Chance generator!");
    }
 
    // Check for !event
    else if (msg.content === "!event") {
 
        // require package
        var datetimePackage = require("node-datetime");
 
        // create 2 variables for the event date
        var nextClanEventDate = datetimePackage.create(eventDate);
        var nextClanEventDateModify = datetimePackage.create(eventDate);
 
        // offset hours appropriate for your server that hosts the bot + local machine
        nextClanEventDateModify.offsetInHours(-7);
 
        // Format both variables into a different date format
        var formatNextClanEventDate = nextClanEventDate.format(format);
        var formatNextClanEventDateModify = nextClanEventDate.format(format);
 
        // Store the current date and time in a variable
        var dateRightNow = datetimePackage.create();
        // format the current date
        var formatDateRightNow = dateRightNow.format(format);
 
        // Convert one of the event date variables and the current date variable so we can compare the dates
        var dateRightNowInMs = new Date(formatDateRightNow);
        var clanEventInMs = new Date(formatNextClanEventDateModify);
 
        // create a variable and store the difference between both dates
        const dateDifference = clanEventInMs - dateRightNowInMs;
 
        // calculate hours and minutes left
        var hoursLeft = Math.floor(dateDifference / hourInMs);
        var remainder = dateDifference - (hoursLeft * hourInMs);
        var minutesLeft = Math.floor(remainder / minuteInMs);
 
        // Create a message array with the correct dates, hours, minutes until event begins
        var msgArray = [
            "Next Clan event date: is " + formatNextClanEventDate + "GMT\n ",
            "The event begins in: " + hoursLeft + "h " + minutesLeft + "m\n ",
            "The event is a test/ WIP"
        ];
 
        // Reply with a message displaying the correct values from the message array
        msg.reply(msgArray[0] + msgArray[1] + msgArray[2]);
    }
 
    // Check for !author
    else if (msg.content === "!author") {
        // reply back a message about the author
        msg.reply("The Owner is @Incursion#9329. \nFor any questions, don't hesitate to ask.\n Submit coding ideas at <https://forms.gle/9NWnGNsuUUwdvfzm9>");
    }
});
 
// Check messages for a specific command
client.on("message", msg => {
    // Send back a reply when the specific command has been written
    if (msg.content === "ping") {
        msg.reply("Pong!");
    }
});
 
// Check messages for a specific command
client.on("message", async msg => {
    // Write if statement if the message includes a specific word
    if (msg.content.includes("!mediumclue")) {
        //Split the string
        var decodeMessage = msg.content.split(" ");
        //The variable with the split string contents is now an array
 
        //Console log the data
        console.log(decodeMessage);
 
        //attempt to convert second item in array to a number
        var correctNumber = Number(decodeMessage[1]);
 
        //Console log the data
        console.log(correctNumber);
 
        //run math.floor on the second index to even out the number.
        correctNumber = Math.floor(correctNumber);
 
        //Console log the data
        console.log(correctNumber);
 
        if (decodeMessage[0] === "!mediumclue" && Number(correctNumber) && correctNumber < 10001 && correctNumber > 0 && decodeMessage.length == 2) {
            var rangerbootsDropRate = 333;
            var wizardbootsDropRate = 666;
            var holysandalsDropRate = 999;
            var itemsFromClue = 0;
            var rollOnTable = 0;
            var totalRangerBoots = 0;
            var totalWizardBoots = 0;
            var totalHolySandals = 0;
 
            // For loop that creates rolls on the medium clue table
            for (var i = 0; i < correctNumber; i++) {
                var itemsEachClue = Math.floor((Math.random() * 3) + 3);
                itemsFromClue += itemsEachClue;
            }
 
            //Log the amount of items from the clue scrolls
            console.log(itemsFromClue);
 
            //For loop each item roll
            for (var i = 0; i < itemsFromClue; i++) {
                rollOnTable = Math.floor((Math.random() * 1000) + 1);
 
                if (rollOnTable === rangerbootsDropRate) {
                    totalRangerBoots++;
                } else if (rollOnTable === wizardbootsDropRate) {
                    totalWizardBoots++;
                } else if (rollOnTable === holysandalsDropRate) {
                    totalHolySandals++;
                }
            }
 
            msg.reply("You opened " + correctNumber + " medium clues.\n And you rolled " + itemsFromClue + " items in total.\n " +
                "And you got " + totalRangerBoots + " Ranger boot(s), " + totalWizardBoots + " Wizard Boot(s), and " + totalHolySandals + " Holy Sandal(s). ");
        }
    }
});
 
// Log in the bot with the token
client.login("insert bot token");
 

