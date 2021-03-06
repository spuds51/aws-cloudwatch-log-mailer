# aws-cloudwatch-log-mailer
Lambda function (python 3.7) that parses cloudwatch log event data and sends relevant log data to SNS topic

![screenshot](https://github.com/davoclock/aws-cloudwatch-log-mailer/blob/master/img/diagram.png)


## Requirements:
1. Lambda function must have the following IAM policy for publishing to SNS:

```
{
    "Version": "2012-10-17",
    "Statement": [
        {
            "Effect": "Allow",
            "Action": "sns:Publish",
            "Resource": "arn:aws:sns:us-east-1:[AWS ACCOUNT ID]:[SNS TOPIC NAME]"
        }
    ]
}
```

## Output Example
![screenshot](https://github.com/davoclock/aws-cloudwatch-log-mailer/blob/master/img/output_example.png)
