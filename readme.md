# Setup for the video api django app

## prerequisite

Generate an api key for the youtube api here:
[google console](https://console.cloud.google.com/apis/api/youtube.googleapis.com/)
and add it to the settings file.

## start the celery consumer

Open a command shell and run:
`celery -A main worker -l INFO -P gevent`

## start the celery producer 

Open a command shell and run:
`celery -A main beat -l info`

## start the project

Open a command shell and run:
`python manage.py runserver`

## endpoints

/list : lists all the videos data in the database, also has filtering, ordering and links of the respective videos  
/search : page to enter the search keyword  
/ : result page for the searches  

## superuser

Username: admin
Password: admin
