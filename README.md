# Postman API Autoamtion Integration with Github Actions #

This repository is a demonstration for POC for integrating postman test with github actions.The test are written in postman and they are executed on the VM with the help of Newman and newman-reported-htmlextra.
Github actions will trigger the project execution on every push to the main branch.You can also execute the project manually using workflow_dispatch.The project runs on a schedule time with the help of cron job.

The HTML report is archieved and ept in the artifact section for the test to download it.Along with that they can the view the report directly from the github page:https://devanjana-22.github.io/Phoenix-inwarranty-flow/
The latest reports is mailed to the team members using gmail SMTP.

## About Me ##
Hi My Name is Devanjana.

## Testing Coverage ##

1.Happy flow testing
2.Negative Testing and Edge case testing
3.Token Testing
4.Data Driven testing with CSV
5.Schema Validation
6.Secrets Management with Github Secrets

## Tech Stack ##
1. Postman
2. Nodejs 22v
3. Newman
4. Newman-reported-Htmlextra
5. Gmail SMTP
6. Github pages
7. CSV for data driven testing
8. AWS_EC2 for self hosted github runner

9. ## Github pages ##
10. You can directly view the latest test report of the postman Test at the Github page Link:https://devanjana-22.github.io/Phoenix-inwarranty-flow/

## HTML Report ##
The report will be created in the newman folder
![Postman Report](https://raw.githubusercontent.com/Devanjana-22/Phoenix-inwarranty-flow/Static-content/Newman%20Report.png)

## Project Structure ##
```
Phoenix inwarrenty flow
├─ inwarrenty-flowcollection Copy.postman_collection.json # Collection file
├─ QA.postman_environment.json # enviornment file
└─ testdata.csv # Test data file

```

 ## How to run the project ##
 You can run the project on your local system:
1.Clone the project on the local system:https://github.com/Devanjana-22/Phoenix-inwarranty-flow.git
2. Install Nodejs and NPM from: https://nodejs.org/en
3. Install Newman :``` npm install -g newman ```
4. Install Newmen-htmlextra:install -S newman-reporter-htmlextra
5.Run the Newman command: 
```
              newman run 'inwarrenty-flowcollection Copy.postman_collection.json' \ 
             -e QA.postman_environment.json \
             -r cli,htmlextra \
             --reporter-htmlextra-export ./newman/index.html
```
