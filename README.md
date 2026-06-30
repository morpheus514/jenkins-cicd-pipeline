\# Jenkins CI/CD Pipeline



A simple Jenkins declarative pipeline that automates build, test, and deployment stages for a Node.js app.



\## Pipeline Stages

1\. \*\*Checkout\*\* — pulls latest code from GitHub

2\. \*\*Build\*\* — installs npm dependencies

3\. \*\*Test\*\* — runs automated tests

4\. \*\*Docker Build\*\* — builds container image

5\. \*\*Deploy\*\* — pushes and deploys the app



\## How It Works

Jenkins is configured with "Pipeline script from SCM" pointing to this repo. The Jenkinsfile defines every stage as code, version-controlled alongside the app.



\## Trigger

Configured with Poll SCM to automatically check for new commits and trigger the pipeline.



\## Tech Stack

Jenkins, Node.js, Express, Docker (build workflow), Groovy (pipeline syntax)

