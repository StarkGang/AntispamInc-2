====================================================
Antispaminc And Telethon
====================================================

Telethon
========
Lets Try To User A User As Soon He Arrives In Chat

.. code-block:: python

  import requests
  from telethon.events import ChatAction
  @client.on(ChatAction)
  async def hmm(event):
    if event.user_joined or event.user_added:
          juser = await event.get_user()
          data = {
            'token': 'yourtokenhere',
            'userid': juser.id
            }
          url = f'http://antispaminc.tk/info/'
          myr = requests.post(url=url, data=data).json()
          if myr['error'] == True:
            await event.reply(f"Welcome, But Something Went Wrong :| \nFull Error : {myr['full']}")
            return
          else:
            if myr['banned'] == True:
                try:
                    await client.edit_permissions(
                    event.chat_id, juser.id, view_messages=False
                  )
                    await event.reply(f"Hello, You Have Been Banned Due To : {myr['reason']}")
                except:
                    pass
            else:
                await event.reply('Welcome To Group')
