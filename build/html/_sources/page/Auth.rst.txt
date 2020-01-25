Auth Method
===========

The otelseasy web service is very easy to integrate with various applications such as web app, mobile app etc. Otelseasy resources can be efficiently accessed by using web service.



The following is a Auth JSON Request.

.. code-block:: html
   :linenos:

   	{
	  "Agent_Code": "Test",
	  "Username": "test-user",
	  "password": "pa$$word"
	}



Auth sample JSON Request.

.. code-block:: html
   :linenos:

   	{
	    "status": true,
	    "message": "Successfull",
	    "token": "eyJ0eXAiOiJKV1QiLCJhbGciOiJIUzI1NiJ9.eyJpZCI6Ijc3IiwiaWF0IjoxNTc5OTI4MTE3LCJleHAiOjE1Nzk5MzAyM"
	}




Auth API Flow
-------------

.. graphviz::

   digraph Flatland {
   
      Client -> Auth_Api -> OE_Product_Database -> OE_Memcache; 
      Auth_Api -> Client;

      Auth_Api  [shape=polygon,sides=4]
      OE_Product_Database  [shape=polygon,sides=4]
   
      Client [peripheries=3,color=yellow];

      OE_Memcache [shape=triangle,peripheries=1,color=blue,style=filled];
      
      }

