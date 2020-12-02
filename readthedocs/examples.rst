====================
Examples Usage
====================
Python
----------
Get Requests
========================================
You Have To Enter Token In Token Parameter And User Id You Wanna Check in userid

.. code-block:: python
   
   import requests
   token = 'TokenHere'
   userids = 1269383181
   url = f'http://antispaminc.tk/info/?userid={userids}&token=' + token
   myr = requests.get(url=url).json()
   if myr['error'] == True:
      print(f"Something Went Wrong \nFull Error : {myr['full']}")
   else:
      if myr['banned'] == True:
          print(f"This User Banned For Reason: {myr['reason']}")
      else:
          print(f"This User is Not Banned")
          
          
Post request
===========================================
You Have To Enter Token In Token Parameter And User Id You Wanna Check in userid

.. code-block:: python

   import requests
   data = {
      'token': 'yourtokenhere',
      'userid': 1269383181
      }
   url = f'http://antispaminc.tk/info/'
   myr = requests.get(url=url, data=data).json()
   if myr['error'] == True:
      print(f"Something Went Wrong \nFull Error : {myr['full']}")
   else:
      if myr['banned'] == True:
          print(f"This User Banned For Reason: {myr['reason']}")
      else:
          print(f"This User Not Banned")
          
PHP
------
Get
=================================
You Have To Enter Token In Token Parameter And User Id You Wanna Check in userids

.. code-block:: php

   <?php
   
   $userids = 1295;
   $token = "yourtokenhere";
   
   echo file_get_contents("http://antispaminc.tk/info/?userid=$userids&token=$token");
   
   ?>


