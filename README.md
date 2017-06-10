# Nagios Task
## INTRO
Hey! This is a nagios task containing an rss feed updates checker, rss feed updates puller(into db), and rss feeds displayer :) (node.js)

### Actions
So what i've done is basically:

* Installed nagios(with dependencies), node 6(with dependencies) & postgres on an EC2 instances
* Created a check in nagios that gets a url and checks for new rss feeds within this url (currently ynet)
* Created a python script to pull the updated feed and insert it to the postgres db
* Created a node.js service that fetches those rss feeds and displays them in a (very ugly) html page.

#### Instructions
* the nagios service is located at: http://35.158.20.35/nagios/
* the service is basically located at the "localhost" host and it is called RSS
* the node service that will display the feeds is at: http://35.158.20.35:3000
* both script & node service are located in on my repo

#### notes
* not meant for production, just a simple poc
