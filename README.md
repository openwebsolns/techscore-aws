# Techscore on AWS

Mostly a CloudFormation template to generate the Techscore application, including:

  * Scores bucket (easy one)
  * S3 bucket for backups (this already exists)
  * CloudFront distribution (US only) for that bucket
  * VPC with public and private subnet
  * RDS cluster and instance in VPC
  * ELB in VPC
  * ACM for private site (ts.$HOSTNAME)
  * ACM for public site (scores.$HOSTNAME)
  * Basion host in public subnet
  * AutoScaling group in private subnet for techscore application
  * IAM Instance Profile for EC2 instance to write to S3 and send e-mail via SES
  * CodeDeploy application and bucket

Also desired are database backups

  * Lambda function for daily backups?


## Scripts

In addition to the templates above, a number of scripts around the AWS
CLI are included:

  * to create/update any of the above templates
  * to SSH into a webserver instance (SSH deserves its own chapter)
  * to stop the bastion host so as to save money
  * **to packgae and deploy the application**
