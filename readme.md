# FuseLess Template

A Template for building CFML powered AWS Lambda Functions.

## Quick Start Instructions

- [Download](https://github.com/foundeo/fuseless-template/archive/master.zip) this repo and unzip it somewhere.
- If you are on a mac / linux run `init.sh` to download Lucee Light and FuseLess jar files. On windows see: [jars/README.md](jars/README.md)
- Add your CFML to the `cfml/app/` folder
- [Install Gradle](https://gradle.org/install/)
- Run `gradle build` in terminal or command prompt

At this point you will now have a CFML serverless application all packaged up in a zip file 🎉 

The zip file is located in `build/distributions/fuseless-template.zip` it can be uploaded to Lambda or tested locally using `sam local`

### Renaming the zip file

In the `build.gradle` file there is a line towards the top that reads:

	archivesBaseName = 'fuseless-template'

Simple rename that, or delete the line and it will use the name of the parent folder. You will also need to update the `template.yml` file, where you see this:

	CodeUri: ./build/distributions/fuseless-template.zip

Change it to match your new zip file name.

### Testing locally 

If you want to test your code locally without uploading to AWS you can use the [**aws sam cli**](https://github.com/awslabs/aws-sam-cli). Once you have installed it, you can simply run:

	sam local start-api

And it will start up a server which you can use to test it on.

You can also use `sam` to generate cloud formation templates to deploy your application. 

### Support, Questions, Issues

[Contact Foundeo Inc.](https://foundeo.com/consulting/coldfusion/) 