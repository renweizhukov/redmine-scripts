# redmine-scripts
All redmine-related scripts.

## backupRedmine

Courtesy of https://www.redmine.org/boards/2/topics/23876.

Back up all redmine wiki entries.

### Schedule the script to run by crontab

Assume that "redmine" is the user which has the execution right to the shell script and the script is saved in /home/redmine/backup. Add the crontab job for the user "redmine".

```
crontab -u redmine -e
```

Then add the following entry if you want to run the back-up job daily.

```
21   01  * * *   cd /home/redmine/backup && ./backupRedmine
```

## createRedmineGitMirrorRepo

Create the mirror git repository in /home/redmine/repos/ and fetch all the commits.