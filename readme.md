# Follow the Sample Deployment instructions

https://eu-west-1.console.aws.amazon.com/codedeploy/home?region=eu-west-1#/first-run/welcome

this will set up a DemoFleet and everything else via CloudFormation

# follow this, to automate stuff

https://aws.amazon.com/blogs/devops/automatically-deploy-from-github-using-aws-codedeploy/


# make a deployment

There are currently 2 different sample commits to show that the deployments actually work

## first commit

    aws deploy create-deployment --application-name DemoApplication --deployment-group-name DemoFleet --deployment-config-name CodeDeployDefault.HalfAtATime --github-location repository=klang/codedeploy-sample,commitId=c5578e82a9f66dd8c02020502982b52edc470c41 --description "one step back" --profile dashsoft --region eu-west-1

## second commit
    aws deploy create-deployment --cli-input-json "$(cat create-deployment.json)" --profile dashsoft --region eu-west-1