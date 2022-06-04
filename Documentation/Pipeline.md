# CircleCi Pipeline

## Steps

1 - It starts after commiting new changes to the master branch
2 - It gets the update then It starts the below `udagram` workflow


## Orbs
    `node: circleci/node@5.0.2`
    `eb: circleci/aws-elastic-beanstalk@2.0.1`
    `aws-cli: circleci/aws-cli@3.1.1`

## Jobs

### Build
1 - node/install\
2 - Checkout\
3 - Install Front-End Dependencies\
4 - Install API Dependencies\
5 - Front-End Lint\
6 - Front-End Build\
7 - API Build

### Confirmation

CircleCi will not proceed to the deployment step unless their is a confirmation from the developer

### Deploy
1 - node/install\
2 - eb/setup\
3 - aws-cli/setup\
4 - checkout\
5 - Deploy App

## Workflow

### udagram

1 - build
2 - hold
3 - deploy