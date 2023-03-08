### POST-MORTEM (INCIDENT REPORT)
	This is an incident report from the malicious attack on project E445 which started on November 22, 2022 [15:09 (WAT)] and was resolved on January 22, 2023 [16:04 (WAT)].
	It’s observed on this day that some of the user details have been compromised and manipulated recently as a result of one or two mistakes from our developers (myself included). After a thorough investigation, it’s discovered that more than 60%  of users details was affected.
	A panel of 6 developers was set up immediately to debug and solve the problem. After thorough debugging and investigation, it’s discovered that the authentication and authorization was the root cause as users details are not properly checked and confirmed before giving access to users’ details and information. The developers happened to check only for authentication and not authorization.
	In the process of authorization, it’s important to check whether a user is logged in or not and retrieves the profile details based parameters. This allows the threat actor(s) to have access to the accounts and administrative privileges.
	After the discovery, the panel (including myself) drew out the next course of action of setting up authorization for the project. We decided to use OAuth 2.0 for both the authentication and authorization. The Authorization Code Flow (ACF) was accessed and understood and a flowchart was drawn. Auth0 was integrated to the app to serve the python flask backend and Augular SPA frontend.
	After this, a test was ran to properly check for the changes made and it came out successful. Then the server was reinstall and the database was updated. It’s then ensured the valid access tokens were ensured to be secured and to prevent possible exposure.
	After making sure of all corrections and all backdoors secured, my team ensured to take a cold coffee to celebrate the achievement and a well deserved break of course.

# Author
Sxamoecode
