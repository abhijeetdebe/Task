# Task of Devops Assembly Line
## Developer
Pushes a web page on the github 
## Jenkins JOB 1
Keeps an eye on the developer branch so when developer updates any file it can download and deploy the webpages on Testing environment.
And here the testing environment is being launched with the help of docker.
This Testing environment is similar to the Production environment.
## Jenkins JOB 2
This job is triggered when job 3 is being successfully build and is stable. Here the task of job 2 is to download and deploy the webpages
on the production environment after job 3 is being successfully build and is stable.
## Jenkins JOB 3
Job 3 is triggered when the QAT or testing team test the web pages that is being deployed on testing environment by the job 1 after
the testing is okay with the web pages and its working on testing environment then they trigger this job and Job 3 Succcessfully merge the
master and developer branch on git hub and trigger the Job 2.
