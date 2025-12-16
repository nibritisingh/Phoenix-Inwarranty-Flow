## Postman API Automation Integration with Github Actions ##
This repository is a demonstration for POC for integrating postman tests with github actions. The Tests are written in Postman and they are executed on the VM with the help of newman and newman-reporter-htmlextra. Github Actions will trigger the project execution on every push to the main branch. You can also execute the project manually using workflow_dispatch. The Projects runs on a scheduled time with the help of the cron job.

The HTML report is archieved and kept in the artifact section for the team to download it. Along with that they can view the report directly from the github page : https://github.com/nibritisingh/Phoenix-Inwarranty-Flow. The latest report is mailed to the team members using GMAIL SMTP.

## About Me ##
Hi my name is Nibriti Singh. I have 5 years of experience in Manual and Automation testing. My Skillset Includes UI Automation with Selenium Webdriver, Cypress, Playwright and for API Testing I use Rest Assured and Postman. You can connect with me over: https://www.linkedin.com/in/nibriti-singh/.

## Testing Coverage ##
1. Happy Flow testing
2. Negative Testing and Edge Case Testing
3. Token Testing
4. Data Driven Testing with CSV
5. Schema Validation
6. Secrets Management with Github Secrets

## Tech Stack ##
1. Postman
2. Nodejs 22v
3. Newman
4. Newman-Reporter-Htmlextra
5. Github Actions
6. Gmail SMTP
7. Github Pages
8. CSV for Data Driven Testing
9. AWS-EC2 instance for self hosted github runner

## Github pages ##
You can directly view the latest test report of the Postman Test at the Github Page Link: https://github.com/nibritisingh/Phoenix-Inwarranty-Flow

## HTML Report ##
The report will be created in newman folder
![Postman Report](https://github.com/nibritisingh/Phoenix-Inwarranty-Flow/blob/static-content/newman-report.png)

## Project Structure ##

Phoenix Inwarranty Flow
├─ Inwarranty-flow Collection.postman_collection.json # Collection File
├─ QA.postman_environment.json #Environment File
└─ testdata.csv # TestData File

## How to run the project ##

You can run the project on your local system for that:

'1. Clone the Project on Local System: https://github.com/nibritisingh/Phoenix-Inwarranty-Flow.git

Install Nodejs and NPM from https://nodejs.org/en

Install ```Newman using npm install -g newman```

Install ```Newman-reporter-htmlextra npm install -g newman-reporter-htmlextra```

Run the Newman Command:

       ```newman run 'Inwarranty-flow Collection.postman_collection.json' \  
      -e QA.postman_environment.json \
      -d testdata.csv \
      -r cli,htmlextra \
      --reporter-htmlextra-export ./newman/index.html```
