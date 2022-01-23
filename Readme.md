# AWS lambda go example

Based on: [aws golang handler docs](https://docs.aws.amazon.com/lambda/latest/dg/golang-handler.html) \
and: [aws golang lambda docs](https://docs.aws.amazon.com/lambda/latest/dg/lambda-golang.html)

## Go
Add github.com/aws/aws-lambda-go/lambda as a dependency\
Build the package with: `GOOS=linux go build main.go` so that it compiles for linux.\
The main.go file needs to have 644 permissions.\
Zip the binary with: `zip function.zip main`


## AWS
Go to the aws lambda function overview page on aws and create a new function\
create a hello world project\
upload the .zip file\
configure the runtime to run with `go1.x` and as Handler use `main`\
go to the test tab and use the `hello-world` trigger and use `main` as the event name\

### AWS Lambda with AWS Api Gateway
When the lambda should be used with Api Gateway The Events need to be of type `events.APIGatewayProxyResponse` of the [github.com/aws/aws-lambda-go/events](github.com/aws/aws-lambda-go/events) library. Find the documentation [here](https://pkg.go.dev/github.com/aws/aws-lambda-go/events#APIGatewayProxyResponse).\
This Example project does not cover APIGateway 