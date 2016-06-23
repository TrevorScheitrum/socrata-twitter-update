# Socrata Twitter Update Application
###Python + flask application that tweets daily updates of new/modified SOCRATA datasets
####Initial version created at the Health 2.0 National Day of Civic Hacking, made available for public use.

This python application checks the metadata of a specified Socrata Open Data Portal and identifies datasets that have are new or have been modified in the last day.  It creates a stack of tweets containing the title and a link to the dataset, then tweets it to Twitter via API.  

We are working to develop a lightweight container for it via Flask and will be posting updates as available; **All collaboration is welcome and appreciated!**

####Usage of Code:
This code expects a local_settings.py (locally) or prod_settings.py (on production server) file in the project directory with a variable called twython_tokens which contains your Twython api tokens, example:

--local_settings.py---

from twython import Twython

twython_tokens = Twython('APP_KEY', 'APP_SECRET', 'OAUTH_TOKEN', 'OAUTH_TOKEN_SECRET')

####Known bugs:
* Does not yet check str len to ensure it is under 140 chars, we are writing code to check and truncate long titles


####Future features:
* Tweet newly created data sets, even if they have not been recently modified
* Tweet data sets with low view counts over time to build a user base
* 
