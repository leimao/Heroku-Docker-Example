# Heroku App Hello Underworld Docker Example

This sample is based on the [Google Cloud Run](https://cloud.google.com/run) [hello-world example](https://github.com/GoogleCloudPlatform/python-docs-samples/tree/7b58dc21f4cfa5042cb0c65884339542746f7b88/run/helloworld). With minimum modification, the sample app could be deployed on [Heroku](https://www.heroku.com/). More specifically, only one additional [`heroku.yml`](heroku.yml) file is required.

## Instructions

### Create Heroku App

[Create a Heroku app](https://dashboard.heroku.com/new-app) called "hello-underworld".


### Install the Heroku CLI

Download and install the [Heroku CLI](https://devcenter.heroku.com/articles/heroku-command-line).

If you haven't already, log in to your Heroku account and follow the prompts to create a new SSH public key.

```
$ heroku login
```

### Create a new Git repository

Initialize a git repository in a new or existing directory.

```
$ git init
$ heroku git:remote -a hello-underworld
```

### Deploy your application

Commit your code to the repository and deploy it to Heroku using Git.

```
$ git add .
$ git commit -am "make it better"
$ heroku stack:set container
$ git push heroku main
```

### View Heroku App

View the Heroku App at [https://hello-underworld.herokuapp.com/](https://hello-underworld.herokuapp.com/).

## References

* [Building Docker Images with heroku.yml](https://devcenter.heroku.com/articles/build-docker-images-heroku-yml)
