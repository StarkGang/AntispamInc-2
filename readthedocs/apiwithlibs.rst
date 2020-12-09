====================================================
Antispaminc And Telethon
====================================================

Telethon
========
Lets Try To Ban A User As Soon He Arrives In Chat.

.. code-block:: python
  
  from antispaminc.connect import Connect
  sclient = Connect('tokenhere')
  @client.on(ChatAction)
  async def ok(event):
    if event.user_joined:
        juser = await event.get_user()
        user = sclient.is_banned(juser.id)
        if user:
            await event.reply(
                f"**#ANTISPAMINC** \n**Detected Malicious User.** \n**User-ID :** `{juser.id}`  \n**Reason :** `{user.reason}`"
            )
            try:
                await client.edit_permissions(
                    event.chat_id, juser.id, view_messages=False
                )
            except:
                pass
        else:
            pass
