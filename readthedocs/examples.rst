====================
Examples Usage
====================
Python
----------

You Have To Enter Token In token Parameter And User Id You Wanna Check in userids

.. code-block:: python
   
   from antispaminc.connect import Connect, TokenNotFound
   token = 'TokenHere'
   userids = 1269383181
   sclient = Connect(token)
   sed2 = sed.is_banned('12974624')
   print(sed2.reason)
   

PHP
------------------
.. code-block:: php

   <?php
   
   $userids = 1295;
   $token = "yourtokenhere";
   
   echo file_get_contents("http://antispaminc.tk/info/?userid=$userids&token=$token");
   
   ?>


