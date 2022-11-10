# Prerequisites for EventBridge Scheduler blog post

This CloudFormation stack builds the prerequisites for the blog post launching EventBridge Scheduler.

[Read the blog post on how to use these prerequistites](https://aws.amazon.com/blogs/compute/introducing-amazon-eventbridge-scheduler/)

In this demo you will see:

- How to create a AWS SNS topic and add an email subscription
- How to create an IAM role and policy that Amazon EventBridge Scheduler can asume to publish messages to SNS when a schedule is triggered.

Important: this application uses various AWS services and there are costs associated with these services after the Free Tier usage - please see the AWS Pricing page for details. You are responsible for any AWS costs incurred. No warranty is implied in this example.

## Requirements

- AWS CLI already configured with Administrator permission
- AWS SAM CLI installed
- NodeJS 16.x installed

## Deploy this demo

Deploy the project to the cloud:

```
sam deploy -g # Guided deployments
```

It will ask you to input a valid email address. This is the email address that will recieve the messages when the schedules are triggered.

When asked about functions that may not have authorization defined, answer (y)es. The access to those functions will be open to anyone, so keep the app deployed only for the time you need this demo running.

The next time when you update the code, you can build and deploy with:

```
sam deploy
```

## Remove the prerequisites

After it is deployed, you should recieve an email in the address you specified as a parameter. Validate that email and then you are ready to continue.

To delete the CloudFormation Stack run:

```
sam delete
```

## Security

See [CONTRIBUTING](CONTRIBUTING.md#security-issue-notifications) for more information.

## License

This library is licensed under the MIT-0 License. See the LICENSE file.
