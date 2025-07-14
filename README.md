# Postman API automation integration with GitHub actions. #

This repository is a demonstration or POC for integrating postman with github actions.
The tests are written in postman and are executed in virtual machine with the help of newman and newman-reporter-htmlextra.
Github actions will trigger on every push of the main branch. Along with that you can execute project manually with workflow_dispatch. The project runs on the scheduled time with the help of the cronjobs.

The reports are archived and are kept in the artifacts section for the team to download, along with that they can view the directory from the github page https://devanshshah95.github.io/Phoenix_in_warranty_flow/
The latest report is mailed to the team members using gmail SMTP.

# Testing Coverage #
1. Happy flows.
2. Data driven testing.
3. Schema validations.
4. Token Testing.
5. Negative Testing.
   
# Tech Stack #

1. Postman
2. NodeJs
3. Newman
4. Newman-reporter-htmlextra
5. Github actions
6. Gmail SMTP
7. AWS-EC2 for self hosted git hub runner
8. Github pages
9. CSV for data driven testing

# Github pages #

You can directly view the project from the URL: https://devanshshah95.github.io/Phoenix_in_warranty_flow/

# HTML REPORT #
![Postman Report](https://github.com/Devanshshah95/Phoenix_in_warranty_flow/blob/Static-Content/newman_report.png)

# How to run the project #

We can run the project manually on the local system.
1. Clone the project on the local system: https://github.com/Devanshshah95/Phoenix_in_warranty_flow.git
2. Install nodeJS, npm and newman.
3. Install newman html extra.
4. Run the newman command:
   newman run Newman_Inwarranty-flow_Collection_Final.postman_collection.json \
             -e QA.postman_environment.json \
             -d testData.csv \
             -r cli,htmlextra \
             --reporter-htmlextra-export ./newman/index.html









