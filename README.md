# AWS-CI_CD
Create AWS-CI_CD pipeline project using AWS CodeCommit, AWS CodePipeline, AWS CodeBuild and AWS CodeDeploy.

![Screen-Shot-2020-09-30-at-6 05 53-PM](https://github.com/Biswajit-Mohapatra2/AWS-CI_CD/assets/105672728/d6597864-fc68-4c7c-8a1b-c331ca391935)



## Create CodePipeline

 In this step, we'll create an AWS CodePipeline to automate the continuous integration process for our Python application. AWS CodePipeline will orchestrate the flow of changes from our GitHub repository to the deployment of our application. Let's go ahead and set it up:

- Go to the AWS Management Console and navigate to the AWS CodePipeline service.
- Click on the "Create pipeline" button.
- Provide a name for your pipeline and click on the "Next" button.
- For the source stage, select "GitHub" as the source provider.
- Connect your GitHub account to AWS CodePipeline and select your repository.
- Choose the branch you want to use for your pipeline.
- In the build stage, select "AWS CodeBuild" as the build provider.
- Create a new CodeBuild project by clicking on the "Create project" button.
- Configure the CodeBuild project with the necessary settings for your Python application, such as the build environment, build commands, and artifacts.
- Save the CodeBuild project and go back to CodePipeline.
- Continue configuring the pipeline stages, such as deploying your application using AWS Elastic Beanstalk or any other suitable deployment option.
- Review the pipeline configuration and click on the "Create pipeline" button to create your AWS CodePipeline.
  
Let's move on to the next step to set up AWS CodeBuild.

## Configure CodeBuild

In this step, we'll configure AWS CodeBuild to build our Python application based on the specifications we define. CodeBuild will take care of building and packaging our application for deployment. Follow these steps:

- In the AWS Management Console, navigate to the AWS CodeBuild service.
- Click on the "Create build project" button.
- Provide a name for your build project.
- For the source provider, choose "AWS CodePipeline."
- Select the pipeline you created in the previous step.
- Configure the build environment, such as the operating system, runtime, and compute resources required for your Python application.
- Specify the build commands, such as installing dependencies and running tests. Customize this based on your application's requirements.
- Set up the artifacts configuration to generate the build output required for deployment.
- Review the build project settings and click on the "Create build project" button to create your AWS CodeBuild project.

  With AWS CodeBuild all set up, we're now ready to witness the magic of continuous integration in action.

  ## Trigger the CI Process

  In this final step, we'll trigger the CI process by making a change to our GitHub repository. Let's see how it works:

- Go to your GitHub repository and make a change to your Python application's source code. It could be a bug fix, a new feature, or any other change you want to introduce.
- Commit and push your changes to the branch configured in your AWS CodePipeline.
- Head over to the AWS CodePipeline console and navigate to your pipeline.
- You should see the pipeline automatically kick off as soon as it detects the changes in your repository.
- Sit back and relax while AWS CodePipeline takes care of the rest. It will fetch the latest code, trigger the build process with AWS CodeBuild, and deploy the application if you configured the deployment stage.

  
