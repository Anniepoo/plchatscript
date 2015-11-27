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

Release
-------

1.0.6   improve failure recovery
1.0.7   chnaged readme, and fixed version
1.0.8   fighting darn pack system
1.0.9 even more fighting darned pack system








