This Script can convert a XAseco2 database into a UASECO database. You just have
to setup the connection data in <settings><mysql> at the config/UASECO.xml file.

UASECO stores for all local records the Gamemode it was running while driving it.
This feature requires it, to setup here your Gamemode which you have used in XAseco2
too. You can find your settings in the MatchSettings file from your dedicated Server
at <playlist><gameinfos><game_mode>:


	+----+------------+
	| ID | Mode       |
	+----+------------+
	|  1 | Rounds     |
	|  2 | TimeAttack |
	|  3 | Team       |
	|  4 | Laps       |
	|  5 | Cup        |
	+----+------------+


Replace the below [GAMEMODE] with one of the above ID. If your ID is not in the
list above, then your Gamemode is not supported by UASECO!

Example: If your dedicated server was running the Gamemode "TimeAttack" then you
have to replace [GAMEMODE] with "2".


After that you can execute this Script from a "Shell" or "Command Prompt",
change into that directory in where you can find uaseco.php.


Linux
~~~~~
php -d max_execution_time=0 -d memory_limit=-1 ./newinstall/database/convert-xaseco2-to-uaseco.php [GAMEMODE]

Windows
~~~~~~~
php.exe -d max_execution_time=0 -d memory_limit=-1 .\newinstall\database\convert-xaseco2-to-uaseco.php [GAMEMODE]
