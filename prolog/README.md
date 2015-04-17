PLChatScript
============

Prolog interface to the ChatScript chatbot engine.

You will need to install ChatScript from

http://chatscript.sourceforge.net/

And run the server by running

C:\docs\chatscript\chatscript.exe port=4050 userlog serverctrlz

on windows or 

chatscript port=4050 userlog serverctrlz

on linux.

set the chatscript address at 

set_chatscript_address(localhost:4050)

then for each user, start a conversation with

start_conversation(someuser, '', Reply) 

the '' is the name of the bot. The '' is the default bot.

then for each volley, use talk/4






