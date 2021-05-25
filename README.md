# books2

Validar el profile:

```
aws sts get-caller-identity --profile demo1
```

Build SAM:

```
sam build --region us-east-1 --profile demo1
```

Package SAM:

```
sam package --template-file template.yaml --s3-bucket demo1-sam-deployment --output-template-file package.yaml --profile demo1
```

Deploy SAM:

```
sam deploy --region us-east-1 --template-file package.yaml --stack-name xxxx --capabilities CAPABILITY_IAM CAPABILITY_NAMED_IAM --profile demo1
```

Listar recursos cloudformation:

```
aws cloudformation list-stack-resources --stack-name demo1-book-stack --profile demo1
```

Borrar stack de cloudformation:

```
aws cloudformation delete-stack --stack-name demo1-book-stack --profile demo1
```


