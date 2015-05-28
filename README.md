# QL-log-parser
Script for real time parsing of Quake Live console logs

This script was created by myself and CaptainTaichou, with the intention to allow a player to simulate the idiosyncratic bot chatter of the Quake3 bot 'Klesk' in Quake Live. The script is written in perl and functions by 'tailing' the qconsole.log file and parsing the file it as the game writes to it. Since Quake Live can't be run in Linux anymore, you'll probably need to run this in Cygwin, unless of course you can find another way to pipe lines to the parser.
You can obviously edit this to fulfill whatever wild functionality you can think of. It's capable of much more than just imitating the klesk bot, but since neither of the creators play Quake anymore we don't really have any further use of it.
And no, this won't get you banned. We notified Syncerror about it, and he didn't really seem concerned. ( He didn't even reply in fact. )

#How to run
To run the script, first move the cfg files to your home/baseq3 directory. Then modify relevant lines in the ql-parselog bash script and the ql-parser.pl script to correctly point to your baseq3 directory. You'll also need to modify the relevant line in the ql-parser.pl file to reflect your player name, it will need this information to correctly interpret relevant lines.
You'll need to put 'seta logfile "3"' in your config file, this will force QL to pipe all console output to the qconsole.log file in your baseq3 directory. 
The ql-parselog bash script will create a symbolic link from your baseq3 directory to the file 'qlcfg', this will be used by the scripts to easily access the files within your baseq3 dir. 
To run the script, just run ./ql-parselog script in your cygwin shell. 
To operate the script in game, simply bind keys to exec the cfg files provided. These will be continually updated as the script parses input.
