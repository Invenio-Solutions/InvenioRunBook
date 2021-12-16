
# Python Deployment
Deployment involves packaging up your web application and putting it in a production environment that can run the app. Python web application deployments are comprised of many pieces that need to be individually configured.

## Deployment hosting options
- "Bare metal" servers
- Virtualized servers
- Infrastructure-as-a-service
- Platform-as-a-service
>The deployer needs to provision one or more servers with a Linux distribution. System packages, a web server, WSGI server, database and the Python environment are then installed. Finally the application can be pulled from source and installed in the environment.

## Deployment tools
- **teletraan** is the deploy system used by the development teams at Pinterest, a huge Python shop!
- **pants** is a build system originally created at Twitter and now split out as its own sustainable open source project.
- **Screwdriver** is an open source build system originally developed at Yahoo! that is now open source. Learn more about it in the introduction post that contains the rationale for its creation.

## Deployment resources
- Automated Continuous Deployment at Heroku explains Heroku's deployment system, the checks they use to ensure code quality and what they have learned from building the pipeline and process.
- Deploying Python web applications is an episode of the great Talk Python to Me podcast series where I discuss deploying web applications based on a fairly traditional virtual private server, Nginx and Green Unicorn stack.
- Thoughts on web application deployment walks through stages of deployment with source control, planning, continuous deployment and monitoring the results.
- Deploying Software is a long must-read for understanding how to deploy software properly.
- The evolution of code deploys at Reddit teaches the history, including the mistakes, that Reddit's development teams learned as they scaled up the development team and the traffic on one of the most-visited websites in the world.
- Deployment strategies defined explains various ways that development teams deploy applications, ranging from reckless to versioned.
- How we release so frequently provides a high-level overview of tactics for how teams at large scale can deploy changes several times per day or more with confidence the systems will not completely fail. There will be bugs, but that does not mean the entire operation will stop.
- Hands-off deployment with Canary explains how SoundCloud automates their deployment process and uses canary builds to identify and roll back issues to mitigate reliability issues that can occur with shipping software at scale.
- Practical continuous deployment defines delivery versus deployment and walks through a continuous deployment workflow.
- 5 ways to deploy your Python application in 2017 is a talk from PyCon US 2017 where Andrew Baker deploys the getting started Flask app using Ngrok, Heroku, Zappa on the serverless AWS Lambda platform, a virtual machine on Google Cloud and Docker.
- Continuous deployment at Instagram is the story of how their deployment process evolved over time from a large Fabric script to continuous deployments. Along the way they encountered issues with code reviews, test failures, canary builds and rollbacks. It's a great read that sheds some light on how Python deployments can be done well at large scale.
- Stack Overflow's guide on how they do deployment is an awesome in-depth read covering topics ranging from git branching to database migrations.
- TestDriven.io shows how to deploy a microservices architecture that uses Docker, Flask, and React with container orchestration on Amazon ECS.