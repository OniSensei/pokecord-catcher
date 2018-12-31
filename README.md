# PokecordCatcher
Paying for an autocatcher for some shitty Pokemon clone on Discord in 2018? haha lol what a joke

This'll catch you all the pokemon that you want, I guess.

## how 2 use

![this one right here](https://i.imgur.com/nL98ALx.png)

Download the latest release. [Release](https://github.com/ExtraConcentratedJuice/pokecord-catcher/releases/)

Keep in mind that if you are updating from an older release, the configuration might've changed. Take a glance at the default configuration included in any new releases and update yours accordingly.

Configure configuration.json. Everthing in there is fairly obvious.

Run the bot.

### How do I run the bot???
Download, install the .NET Core runtime from [HERE](https://www.microsoft.com/net/download/thank-you/dotnet-runtime-2.1.1-windows-hosting-bundle-installer)

Navigate to your bot directory and open a command prompt, then run this command:

`dotnet PokecordCatcher.dll`

After that you'll have the bot catch Pokemans for you xd

### OK now I have these cool pokeman hax but how do I filter stuff???
there are built in commands and stuff to help you do that

set OwnerID and UserbotPrefix in config.json first, YOU SHOULD HAVE IT CONFIGURED. If you're confused on whether to include quotes or not, check the example configuration.

Add pokemon names to WhitelistedPokemon if you want to filter to certain pokemon, add guild IDs to WhitelistedGuilds if you want to limit the bot to certain servers.

### Commands

You can toggle the bot's filtering with some commands.

`<prefix>` is the prefix that you set for Userbot in config.json

`<prefix>status` - displays the bot's toggled properties

`<prefix>reload` - reloads config.json 

`<prefix>toggleguilds` - toggles guild whitelisting

`<prefix>togglepokemon` - toggles pokemon whitelisting

`<prefix>togglespam` - toggles the bot's built in spammer

`<prefix>echo <message>` - has the bot say something

`<prefix>display <pokemon name>` - has the bot display pokemon of the supplied name

`<prefix>trade <pokemon name>` - has the bot trade all of its pokemon of the supplied name

`<prefix>tradebyid <pokemon id>` - has the bot a pokemon with the supplied ID to you


your settings will persist accross restarts

### Configuration Documentation

Don't copy this shit into your config, it won't work because json doesn't support comments lol just use it as a reference

```javascript
{
	// This is your user token. Use google to figure out how to get it.
	"Token": "ur user token here xd",
	// This is the prefix for the pokecord bot.
	"PokecordPrefix": "-",
	// This is the prefix that you will use to issue commands to your userbot.
	"UserbotPrefix": "&",
	// This is your Discord user ID. Use google to figure out how to get it. All commands be executed by a user with this ID only.
	"OwnerID": 6969696969696,
	// If the bot should log catch success/fail
	"EnableLogging": true,
	// Enables a response after catching to mock people xd just disable this if you don't want it to respond
	"EnableCatchResponse": false,
	// The catch response
	"CatchResponse": ":joy: :ok_hand: LE POKEMANS XDXD",
	// A list of pokemon that the bot should only catch while in pokemon whitelist mode
	"WhitelistedPokemon": ["Rayquaza", "Mew", "Shaymin", "Bidoof", "Starly", "MEME"],
	// The minimum delay in MILISECONDS for a catch
	"CatchMinDelay": 500,
	// The maximum delay in MILISECONDS for a catch
	"CatchMaxDelay": 1000,
	// The ID of the channel you want the spammer to send messages to.
	"SpamChannelID": 696969696969,
	// Minimum delay in MILISECONDS for the spammer.
	"SpammerMinDelay": 3000,
	// Maximum delay in MILISECONDS for the spammer.
	"SpammerMaxDelay": 4500,
	// Messages for the spammer to send. Selected randomly.
	"SpammerMessages": ["david has 10 bowling balls", "my name jeff", "THE PAIN", "SAVE ME"],
	// Guilds that the bot should listen on only when in guild whitelist mode
	"WhitelistedGuilds": [696969696969, 420420420420]
}
```

### FAQ
Q: yo why is the bot recognizing some pokemon as other pokemon

A: I scraped the shit out of bulbapedia for the pokemon list so it isn't perfect, just use the hashing tool to hash and add pokemon to poke.json

------

Q: something isnt working help pls

A: check all of the issues on the repo for your problem, if you can't find one then make one

------

Q: goddamn this autocatcher sucks wtf

A: yeah i know lol how about you make it better by submitting a pull request huh

------

Q: guild whitelisting/pokemon whitelisting/spammer doesn't work??!?!?!!?!

A: check out the command reference above. use the toggle commands.

### Edits by xzydrate
![main bot window](https://i.imgur.com/UBw53lF.png)
![settings window](https://i.imgur.com/qPaNwfu.png)
-----
This is just a UI addon coded in VB.NET. It runs the output of the cmd/powershell in a rich text box and filters the data recieved to highlight different colors based on what the bot is doing. It will also filter your seen/caught into another richtextbox. 

It uses this method to also track how many pokemon you've seen, caught, skipped, failed to catch or which were legendary. As well as export the list of caught/seen to a text file that you can search through with ease.

When the bot is started it also keeps track of its run time, and allows you to edit your config.json file.

The dev button was just so i could see if things worked or didnt work essentially. It does however log the time and which pokemon that may have spawned as legendary to make things easier.

I have been working on fixing the poke.json to include what is missing, however they're not all working and im still continuing to try.
