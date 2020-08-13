## Prerequisites

Please make sure you have Nodejs installed. You can get it [here](https://nodejs.org/en/).

## Install

```bash

# If you don't already have the serverless cli installed, do that
npm install -g serverless
# Clone this repo
git clone git@github.com:normanwongcl/whatsapp-notification.git

# cd into project and set it up
cd whatsapp-notification

```

## Development

Creating and deploying a new function takes two steps, which you can see in action with this repo's default Hello World function (if you're already familiar with Serverless, you're probably familiar with these steps).

#### Add your function to `serverless.yml`

In the functions section of [`./serverless.yml`](./serverless.yml), you have to add your new function like so:

```yaml
functions:
  hello:
    handler: hello/index.handler
```

You can see here that we're setting up a function named `hello` with a handler at `hello/index.js.

## Deployment

Assuming you've already set up your default AWS credentials (or have set a different AWS profile via [the profile field](serverless.yml#L26):

Then run the command below:

```bash
serverless deploy
```

Test function is working

```bash
serverless invoke --function hello
```
