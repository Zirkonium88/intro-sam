# Steps

sam package \
  --template-file template.yml \
  --output-template-file cognito_package.yml \
  --s3-bucket mw-800524020870-example

sam deploy \
  --template-file cognito_package.yml \
  --stack-name sam-demo-cognito \
  --capabilities CAPABILITY_IAM

sam local invoke HelloWorldFunction
