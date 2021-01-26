Greetings users!

My name is D3FAULTJ3ST3R and I programmed this bot in my free time.
I hope this bot does everything you would like it to do. If you
have any questions about my program or perhaps any of my other work,
you can reach me on any social @D3FAULTJ3ST3R.

Steps To Get The Bot Working

1. Please ensure to modify the *Auth.js files to have the correct OAuth
tokens and passwords as needed.

2. Please check to be sure that the timer variables are set to what you
would prefer them to be set to.

3. Ensure that the discord channel variables and twitch channel variables
are also set to the correct settings for your servers.

4. Be sure to set up a MYSQL server of some sort to connect to and provide
the needed credentials to your auth files.

5. Be sure to have both Node.js and NPM installed on your machine and the
required libraries: tmi.js, mysql.js, discord.js, string-similarity.js, request.js.

6. Run the js file with node.js and enjoy!

MYSQL Server Setup!

For Windows systems, checkout programs like WAMP that run sudo servers
on your local machine. This will create and run an instance of a few things
such as a webhost, MYSQL server and MariaDB instance. You can look
more into WAMP on their site or through videos.

For Linux systems, simply install MYSQL and run it locally. Look for
instructions on this through Youtube or other means.

For MAC systems, simply install MYSQL and run it locally. Look for
instructions on this through Youtube or other means.

I suggest to use a program like DBeaver to manage these databases and tables
as it is the easiest way to do so since DBeaver provides an excellent GUI
and way to interact and control your database and even create this info.

You can even generate whole tables using CSV files or convert tables to CSV files.
This is why I provided a csv for the questions to transport in the jeopardy tables
or be used to create the jeopardy table.

Table layouts are as follows and you can even use the insert calls below:

jeopardy {
	id - int - unique - auto
	show_number - int
	air_date - var
	round - var
	category - var
	value - var
	question - var
	answer - var
	used_both - int
	used_twitch - int
	used_discord - int
}

jeopardy_players_twitch {
	playerid - int - unique - auto
	name - var
	money - int
}

jeopardy_players_discord {
	playerid - int - unique - auto
	name - var
	money - int
}

Commands to create tables via commandline:

jeopardy:

CREATE TABLE `jeopardy` (
	`id` INT NOT NULL AUTO_INCREMENT,
	`show_number` INT,
	`air_date` VARCHAR,
	`round` VARCHAR,
	`category` VARCHAR,
	`value` VARCHAR,
	`question` VARCHAR,
	`answer` VARCHAR,
	`used_both` INT DEFAULT '0',
	`used_twitch` INT DEFAULT '0',
	`used_discord` INT DEFAULT '0',
	PRIMARY KEY (`id`)
);

jeopardy_players_twitch: 

CREATE TABLE `jeopardy_players_twitch` (
	`playerid` INT NOT NULL AUTO_INCREMENT,
	`name` VARCHAR NOT NULL,
	`money` INT NOT NULL DEFAULT '0',
	PRIMARY KEY (`playerid`)
);

jeopardy_players_discord:

CREATE TABLE `jeopardy_players_discord` (
	`playerid` INT NOT NULL AUTO_INCREMENT,
	`name` VARCHAR NOT NULL,
	`money` INT NOT NULL DEFAULT '0',
	PRIMARY KEY (`playerid`)
);

Quick Overview

This bot is able to run trivia in both Discord and Twitch simultaneously.
You can choose to run it synchronously or asynchronously. You can also
choose to run it separately while also be synchronously ran. (This means
you can decide whether to have discord and Twitch both compete for the
answer or if you'd prefer they be separate but still the same questions.)

If you have either one deactivated, it will run in async mode to avoid
sync mode being broken.

There will be more detailed notes below on the different parts of the
program. Most of everything you could need to customize, is up at the
top of the program.

If you enjoy this bot and would like to help support my work, consider
donating to me: paypal.me/d3faultj3st3r

Disclaimer

Please be aware that while this code is open to modification or
use for free; I ask that you not attempt to modify and then sell my
code. I'm making this program free and open to modification in the
first place with hopes that people will be able to use my base as
the platform to customize a trivia bot to their liking. Not to
upstage my creation and make a buck off of others who don't know.
I'm open to making changes and helping people work on customizing
the bot to do as they please. So if you ever want changes to be
made or think there is improvements to be made, I'd ask that you
reach out to me instead.
