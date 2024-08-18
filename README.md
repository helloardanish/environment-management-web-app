## Environment management (Web-App)

### A web app to manage your deployments(multiple services) in very easy way. One place to know whoever is deploying, whoever is testing, whoever is waiting in the queue for deployments.

Please see the issues to know why this web-app is developed and which problem it solves [Problems](#issues).

Tools used:  
![Static Badge](https://img.shields.io/badge/docker-latest-red)
![Static Badge](https://img.shields.io/badge/java-21-blue)
![Static Badge](https://img.shields.io/badge/maven-3.9.8-red)
![Static Badge](https://img.shields.io/badge/node-22-red)
![Static Badge](https://img.shields.io/badge/Angular-18-red)
![Static Badge](https://img.shields.io/badge/mongo_db-latest-orange)
![Static Badge](https://img.shields.io/badge/mongo_express-latest-orange)


![alt text](image/1000.png)

#### Add a user:
Enter name, description(why you require server), expected time and click add me:
![alt text](image/1001.png)

Because no one was testing queue is assigned to you.
![alt text](image/1002.png)

#### What if another people added?
![alt text](image/1003.png)

He/she will be waiting in queue unless the first one is not completed the testing on server.

#### And so on
![alt text](image/1004.png)


#### If any person completed the testing, queue will be assigned to next user(Once user completed his testing he/she can click testing completed button).
![alt text](image/1005.png)

Queue will be assigned to next user(here, Murad)
![alt text](image/1006.png)

#### But what if some urgent testing is required? Well, then you can choose urgent option. For that admin access will be required, admin can be set up in database by the person hosting it on the server(Please see Adding-Admin-Users.md file).


###### Enter the details for the urgent testing.
![alt text](image/1011.png)
But urgent checkbox is disabled, you see urgent button below right? Click and validate ad admin by entering admin credentials:
![alt text](image/1012.png)

If the credentials are correct, checkbox should be enabled!
![alt text](image/1013.png)

###### Now because it is a production issue and urgent testing required, once you click add current user(Murad) will be freezed and queue will be assigned to urgent user!
![alt text](image/1014.png)

Once the production issue will be resolve and mark as testing completed, queue will follow the same order, it will be assigned back to Murad and then Aman unless if urgent testing comes in between again.
![alt text](image/1015.png)

#### If large no of users are added in queue it will not be good to scroll or go through pages to check who is testing, so you can use filter options:
![alt text](image/1016.png)

Completed will show the user who have completed the testing:
![alt text](image/1017.png)

Testing will always show a single user who is currently testing:
![alt text](image/1018.png)

Waiting will show the user who are waiting for deployment and testing:
![alt text](image/1019.png)


##### Please note, at one time, only 1 urgent testing is possible!


### Issues

After working in few companies, I see this challenge everywhere. Whenever we have to deploy over the server(talking about dev but can be used for UAT/production as well) we have to ask our colleagues and lots of senior persons that if someone is deploying and testing currently on the server. Same things is managed most of the times with groups over teams/whatsapp/meet. It works well when we have very few developers who requires testing in a day but managing goes out of hand when the number of developers who wants to deploy and test increases.

![alt text](image/1022.png)

![alt text](image/1023.png>)

 

As we can see from the above group messages that even with few team members(10-20) it is very hard to scroll thorugh all the messages and know whoever will test next and whoever is testing. This issue not in single place but in most of the place and as a developer these things are very irritating to go throgh and find who was testing by focusing on each single messages of the group and really hard to manage for how many turns I'll get the queue.

This web-app solves this problem. Now developers who wants to deploy can see in 1 click whether the deployment queue is available or after whom I can test. They can also see who completed their testing after deployments and who is testing currently and who all are waiting in the queue in 1 click only.


#### Because it resolves the developer issues, I've made is open source for you guys.
#### To use this web-app in your system, please open Run-App.md

[Run App In My System](Run-App.md)


#### Please keep an eye on docker images for frontend and backend services of this app.

[Frontend-docker hub](https://hub.docker.com/repository/docker/helloardanish/environment-management-frontend/general)
--
[Backend-docker hub](https://hub.docker.com/repository/docker/helloardanish/environment-management-backend/general)

#### Suggestions are always welcome to make this more better and useful for the future deployments managements. Please raise the issue.

## Happy Coding,
### A R