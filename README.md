# Techscore on AWS

Mostly a CloudFormation template to generate the Techscore application, including:

  * Scores bucket (easy one)
  * CloudFront distribution (US only) for that bucket
  * VPC with public and private subnet
  * RDS cluster and instance in VPC
  * ELB in VPC
  * ACM for ts.collegesailing.org
  * ACM for scores.collegesailing.org
  * Basion host in public subnet
  * EC2 instance in private subnet for techscore application
  * IAM Instance Profile for EC2 instance to write to S3 and send e-mail via SES

Also desired are database backups

  * Lambda function for daily backups?
  * S3 bucket for backups (this already exists)
