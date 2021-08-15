# AWS lambda go example

Based on: https://docs.aws.amazon.com/lambda/latest/dg/golang-handler.html
and: https://docs.aws.amazon.com/lambda/latest/dg/lambda-golang.html

Add github.com/aws/aws-lambda-go/lambda as a dependency  
Build the package with: `GOOS=linux go build main.go` so that it compiles for linux.  
The main.go file needs to have 644 permissions.  
Zip the binary with: `zip function.zip main`


## AWS
Go to the aws lambda function overview page on aws and create a new function  
create a hello world project  
upload the .zip file  
configure the runtime to run with `go1.x` and as Handler use `main`  
go to the test tab and use the `hello-world` trigger and use `main` as the event name  

