========================
ANTI SPAM INC API
========================

Get Request
===========================================
.. code-block:: python

   import requests
   token = 'yourtokenhere'
   userids = <UseridHere>
   url = f'http://www.NoSpamPlus.ml/info/?userid={userids}&token=' + token
   myr = requests.get(url=url).json()
   if myr['error'] == True:
      print(f"Something Went Wrong \nFull Error : {myr['full']}")
   else:
      if myr['banned'] == True:
          print(f"This User Banned For Reason: {myr['reason']}")
      else:
          print(f"This User Not Banned")


Post request
===========================================
.. code-block:: python

   import requests
   data = {
      'token': 'yourtokenhere',
      'userid': <queryidhere>
      }
   url = f'http://www.NoSpamPlus.ml/info/'
   myr = requests.get(url=url, data=data).json()
   if myr['error'] == True:
      print(f"Something Went Wrong \nFull Error : {myr['full']}")
   else:
      if myr['banned'] == True:
          print(f"This User Banned For Reason: {myr['reason']}")
      else:
          print(f"This User Not Banned")
          
=============
What is this?
=============

`| Telegram is a popular messaging application But is Full Of Spammers and Scammers.
| We Have A Mission To Make Telegram Free of These People. So we Have Made NoSpamPlus Api.
| Usage is Very Simple, Read Below To Know More !`
