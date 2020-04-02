# AWS CLI Using Docker

## Prerequisite

- AWS account setup and ready
- Access Key and Access ID handy

## Steps
1.  Configure the aws cli using docker image
<br>`docker run --rm -it -v ~/.aws:/root/.aws amazon/aws-cli configure`<br>
**--rm** Remove the container once it is executed<br>
**--it** Enables the interactive shell<br>
**-v** Mount the user directory where .aws will be created on the root/.aws of the container<br>
**configure** Enable aws cli to configure the first time settings<br>
   - Configure command will ask for
      - AWS Key
      - AWS ID
      - Default Region
      - Output format
2. Execute AWS commands
<br>`docker run --rm -it -v ~/.aws:/root/.aws amazon/aws-cli s3 ls`<br>
