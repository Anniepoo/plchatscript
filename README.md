PLChatScript
============

Prolog interface to the ChatScript chatbot engine.

You will need to install ChatScript from [here](http://chatscript.sourceforge.net/)

And run the server by running

   =|C:\docs\chatscript\chatscript.exe port=4050 userlog serverctrlz|=

on windows or 

   =|./LinuxChatScript64 port=4050 userlog serverctrlz|=

on linux.

Note that on Linux you'll need SWI-Prolog 7.3.0 or better,

set the chatscript address at 

    set_chatscript_address(localhost:4050)

then for each user, start a conversation with

    start_conversation(someuser, '', Reply) 

the '' is the name of the bot. The '' is the default bot.

then for each volley, use `talk/4`

Deploying a new Release
-----------------------

1. make your local changes
2. change this file by adding a description of your release on last line
3. change pack.pl to use the new release number
4. commit changes locally
5. add tag to commit (git tag x.y.z)
6. git push origin master
7. download the appropriate archive from github:  https://github.com/Anniepoo/plchatscript/archive/1.0.8.zip
You can also make your own archive. USE ZIP, NOT bz or gz
structure inside the zip MUST be:
plchatscript -+
              + README.md
              + pack.pl
              + prolog - +
                         + chatscript.pl
                         + license.txt

this is how github makes the archive, so using theirs is convenient

8. Upload this archive to /var/www/packs on www.pathwayslms.com
9. run SWI-Prolog
10. ?- pack_install('http://pathwayslms.com/packs/plchatscript-1.0.8.zip').   <-- with whatever version your making


Release
-------

1.0.6   improve failure recovery
1.0.7   chnaged readme, and fixed version
1.0.8   fighting darn pack system
1.0.9 even more fighting darned pack system








