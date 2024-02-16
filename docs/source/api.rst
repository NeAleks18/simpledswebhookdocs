API
=====

.. _start:

How to use the API?
------------

It's very simple, just add an Empty (Create Empty) and add the DiscordWebhookAPI component (Script). This will be your API controller

Also, forgot to add token and id via Inspector.


.. _sendmsg:

Send Message
------------

.. code-block:: csharp

   public void SendMessage(bool debug, string content, string username = null, string avatar_url = null, bool tts = false)

Let's understand the function directly from the API code itself. 

WHAT IT IS, WHY SOME VARIABLES ARE ALREADY LABELED...
Don't be frightened, it means it's not important and can be written without labeling.

And how do I jump username and change only avatar_url?
It's very easy, just write null where string format and bool where bool, put as in the example above, that way you just jump.

Why no EMBED?
For now it's a scary thing for me, in the future it will be.

What is the bool debug?
This is debug, i.e. when you call the function, it will log failures or successes in the console in parallel

.. note::

   I recommend that before using the API and your script itself for the first time, DEBUG should be used first to detect problems.

.. _getmsg:

Receiving a message (From webhook only)
------------

.. code-block:: csharp

   public string GetMessage(string msgid)

Let's break down the function directly from the API code itself. 

What is msgid?
msgid - MessageID, the ID of the message from the webhook whose data you want to retrieve.

How do we use it?
As a variable, it returns a string with the JSON code from Discord.

.. _editmsg:

Changing the message (From webhook only)
------------

.. code-block:: csharp

   public void EditMessage(bool debug, string msgid, string content)

Let's analyze the function directly from the API code. 

Stop, why do we need to parse it, it seems to be clear, we have parsed everything here earlier, if you still have questions, write to me.

.. _deletemsg:

Deleting a message (From webhook only)
------------

.. code-block:: csharp

   public void DeleteMessage(bool debug, string msgid)

Let's analyze the function directly from the code of the API itself. 

Everything is clear here too, well, in principle, these are all functions.
