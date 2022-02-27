# musician-app
NodeJS / React sample app for AWS CI/CD pipeline tutorial

https://www.youtube.com/watch?v=NwzJCSPSPZs

**Step1:**
 Services >> aws elasticbeanstalk
Name--musician-app
platform--Nodejs
sample app >> Create application 

**Step2**
Services >> Aws pipeline 
Create pipeline 
Name--musician-app-pipeline 
New service role 
default location, next 
Source - github - connect github 
repo-- select 
branch - select (main/master)
github methods 
build stage - skip 
deploy stage -- elastic bean stalk region - ap-south-1
app name-- musician-app
env - select

**Step3**
After successfull deployment , copy env id (url) from elasticbeanstalk and check website on any browser , You will see your app deployed 
Now, make some changes in code in repo 
muscian-app >> route >> musician.js 
content --- add health check  which return 200 ok response 
save the changes 

Now, As soon as you make changes in code , it will trigger pipeline automatically and deploy new code to your env 
copy url and check it by /musician/health in url 
 
**Step4**
Delete the resources , delete env in elasticbeanstalk and pipeline 
