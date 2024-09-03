# AWS estimated charges email notification

CloudFormation template to send an email notification when the estimated monthly
charges exceed a configured threshold. The template creates creates an AWS budget to monitor the estimated charges and send an email when it detects
estimated charges exceed the threshold.

## Configuration

Modify `params.example.json` with your desired values and rename the file to
`params.json`.

## Deploy

To create the initial CloudFormation stack, run the command below from the root
of the repository:

```console
aws cloudformation create-stack --stack-name EmailAlerts --template-body file://src/budget.yml --parameters file://params.json
```

To update the stack, run the command below from the root of the repository:

```console
aws cloudformation update-stack --stack-name EmailAlerts --template-body file://src/budget.yml --parameters file://params.json
```

## License

MIT
