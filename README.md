# Postman API Automation Integeration with GItHub Action #
This repository is demonstaration for POC for integerating Postman tests with github action.the tests are written in Postman and they are exceuted on VM with the help of newman and newman -reporter-htmlextra.
Github actons will trigger project execution on every push to the main branch.Along with that Workflow_dispatch is used to exceute project manually.The projects run on scheduled time with the help of CRON job.

The HTML reports are archieved and kept in artifacts section for the etam to download.Along with that they can view report directly from the github page:https://manpreet-90.github.io/Phoenix-Inwarranty-flow/
The latest report is mailed to team member using gmail smtp.

## About Me: ##
My name is Manpreet Kaur.I have approx 2 years of experience of automation Testing and my skillset inludes UI automation with selenium webdriver with java and for API testing using Rest Assured.
You can connect with me (https://www.linkedin.com/in/manpreet-kaur-5572221a4/)

## Testing Coverage ##
1.Happy Flow Testing

2.Negative Tetsing and edge case Testing

3.Token testing 

4 Data driven testing with CSV

5.Schema Validation

6.Secrets Managemnt with GitHub Secrets

# TechStack #
1.Postman

2.newman

3.newman-reporter-htmlextra

4.nodejs

5.github Actions

6.Gmail SmTp

7.GitHub Pages

8.Csv for Data Driven testing

9.AWS EC2 Instance for Self hosted GitHub Runner

## GitHubPages ##
You can directly view test report of Postman test of GithUb Page link:https://manpreet-90.github.io/Phoenix-Inwarranty-flow/

## Project Structure ##

```
InWarrantyFlow
├─ InWarrantyFlow TestData.postman_collection.json ##collection File
├─ QA.postman_environment.json  ## environment File
├─ README.md
└─ TestData.csv  ## test Data File

```

## How to run the project ? ##

You can run the project on your local system for that :

1.Clone the project on local system:https://github.com/Manpreet-90/Phoenix-Inwarranty-flow.git

2.Install nodejs and npm :https://nodejs.org/en

3.Install newman using npm: ```npm install -g newman ```

4.Install ``` npm install -g newman-reporter-htmlextra ```

5.Run the newman commmand:
```
            newman run "InWarrantyFlow TestData.postman_collection.json" \
            -e "QA.postman_environment.json" \
            -d "TestData.csv" \
            -r cli,htmlextra \
            --reporter-htmlextra-export ./newman/index.html
```

## HTML Report ##
The reprt will be created in newman folder:
![POstman Report](https://github.com/Manpreet-90/Phoenix-Inwarranty-flow/blob/Static_content/newman%20report.png)



