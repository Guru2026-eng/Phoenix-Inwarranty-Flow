# Postman API Automation Integration With Github Actions #
This repository demonstrates a POC for integrating Postman tests with GitHub Actions.The tests are created in Postman and executed on the VM with the help of Newman and newman-reporter-htmlextra.
GitHub Actions triggers the test execution automatically on every push to the main branch. The tests can also be executed manually using workflow_dispatch.

The project is also configured to run automatically at a scheduled time using a cron job.

Test Reports : The HTML test report is archived and stored in the GitHub Actions Artifacts section, allowing team members to download and review it.
The latest test report can also be viewed directly from the GitHub Pages site: https://guru2026-eng.github.io/Phoenix-Inwarranty-Flow/

Email Notification : The latest HTML test report is emailed to the team members using Gmail SMTP after the test execution is completed.

## About Me ## 
Hi, I'm Gurudatta Umbarkar, a QA Automation Engineer with 4.5 years of experience in software testing and test automation.
I have hands-on experience in Java, Selenium, TestNG, Cucumber, Playwright, JavaScript, REST API testing, Postman, RestAssured, SQL, Git, Jenkins, Docker, and GitHub Actions.
I use this GitHub repository to showcase my test automation projects, POCs, API testing frameworks, CI/CD integrations, and automation solutions.
I am passionate about building reliable, scalable, and maintainable test automation frameworks and continuously improving testing processes through automation.

## Testing Coverage ##
1) Happy Flow Testing
2) Negative and Edge case testing
3) Token Testing
4) Data Driven Testing using CSV file
5) Schema Validation
6) Secrets management with Github Secrets

## Tech Stack ##
1) Postman
2) Javascript
3) Nodejs v22
4) npm
5) Newman
6) newman-reporter-htmlextra
7) Github Actions
8) Github Pages
9) CSV for data driven testing
10) AWS-EC2 instance for self hosted github runner

## Github Pages ##
You can directly view the latest test report of the Postman Test at the Github Page link : https://guru2026-eng.github.io/Phoenix-Inwarranty-Flow/

## HTML Report ##
The Report will be created in the newman folder
![Postman Report](https://github.com/Guru2026-eng/Phoenix-Inwarranty-Flow/blob/static-content/NewmanReport.png)

## Project Structure ##
```
Phoenix Inwarranty Flow
├─ InWarrentyFlowCollection With Newman CLI.postman_collection.json  // Collection File 
├─ QA.postman_environment.json // Environment File
└─ testdata.csv // Test Data File

```

## How to Run the Project ##
You can run the project locally by following the steps below:
1. Clone the Repository to your local system: https://github.com/Guru2026-eng/Phoenix-Inwarranty-Flow.git
2. Download and install Node.js and NPM from: https://nodejs.org/en
You can verify the installation using:
 1) ``` node --version ```
 2) ``` npm --version ```
3. Install Newman globally using NPM: ``` npm install -g newman ``` & Verify the installation: ``` newman --version ```
4. Install the newman-reporter-htmlextra package globally: ```npm install -g newman-reporter-htmlextra```
5. Run the Postman collection using the following command:
   ```
                newman run 'InWarrentyFlowCollection With Newman CLI.postman_collection.json' \
                -e QA.postman_environment.json \
                -d testdata.csv \
                -r cli,htmlextra \
                --reporter-htmlextra-export ./newman/index.html
   ```
7. Parameters Used : 
-e — Specifies the Postman environment file.
-d — Specifies the CSV test data file.
-r cli,htmlextra — Generates both CLI and HTML Extra reports.
--reporter-htmlextra-export — Specifies the location where the HTML report will be generated.

After execution, the HTML report will be available at: newman/index.html




