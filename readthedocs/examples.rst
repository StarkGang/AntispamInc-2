====================
Examples Usage
====================
Python
----------

You Have To Enter Token In token Parameter And User Id You Wanna Check in userids

.. code-block:: python
   
   from nospamplus.connect import Connect
   mytoken = 'your_token_from_@nospamplusbot'
   token_connect = Connect(mytoken)
   user = token_connect.is_banned(12974624)
   print(user.ban_code)
   print(user.reason) 
   

PHP
------------------
.. code-block:: php

   <?php
   
   $userids = 1295;
   $token = "yourtokenhere";
   
   echo file_get_contents("http://NoSpamPlus.tk/info/?userid=$userids&token=$token");
   
   ?>


