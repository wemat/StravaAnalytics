# StravaAnalytics

Strava collects a lot of data and has a great API. Let's use this API and analyze the data with Python. 

If you want to reproduce this usecase follow this steps:

Note: I used Postman for this part. 
There is an excellent video on this here: 
https://www.youtube.com/watch?v=sgscChKfGyg&list=PLO6KswO64zVvcRyk0G0MAzh5oKMLb6rTW&index=1

1. Get a strava developer account (you can ask for it in you strava account) 

2.  paste in YOUR client id in the following link. Authorize the app. 
http://www.strava.com/oauth/authorize?client_id=CLIENT_ID&redirect_uri=http://localhost&response_type=code&scope=activity:read_all
-->It will look like it didn't work but in the browser bar there will be a new token (CODE). Copy that token and paste it in step 3. 

3.exchange authorization code for access & refresh token 
https://www.strava.com/oauth/token?client_id=31638&client_secret=CLIENT_SECRET&code=CODE&grant_type=authorization_code

4. (optional) view activities using the new access token
https://www.strava.com/api/v3/athlete/activities?access_token=ACCESS_TOKEN


5. use refresh token to get new access token (refresh token stays the same) 
https://www.strava.com/oauth/token?client_id=31638&client_secret=8dc46386530518924b77b005ce38fde7bee2f920&refresh_token=cb714ed952acbfe299245b26bf852552a183008a&grant_type=refresh_token

6. Put the client id, client_secret and refresh_token in the text file "api_params". 

7. Run the Notebook. 
