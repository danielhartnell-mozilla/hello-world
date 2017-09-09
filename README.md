# hello-world
Building Continuous Deployment on AWS with AWS CodePipeline, Jenkins and AWS 
Elastic Beanstalk

Source: https://aws.amazon.com/blogs/devops/building-continuous-deployment-on-aws-with-aws-codepipeline-jenkins-and-aws-elastic-beanstalk/

## Summary

This sample application will act as a baseline as I continue to learn more 
about deploying applications to AWS with their native tools like CodeBuild, 
CodePipeline and Elastic Beanstalk.

For this simple Node application, we take advantage of CodeBuild and a 
corresponding `buildspec.yml` file.

```
version: 0.2

phases:
  build:
    commands:
      - echo Build started on `date`
      - echo Running npm install
      - npm install
  post_build:
    commands:
      - echo Build completed on `date`
artifacts:
  files:
- "**/*"
```
