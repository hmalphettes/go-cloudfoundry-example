# Example Golang Application for Cloud Foundry V2

Based on [Go on Heroku](https://gist.github.com/kr/299535bbf56bf3016cba).

## Requirements

* A Cloud Foundry account targetting [run.pivotal.io](http://docs.cloudfoundry.com/docs/dotcom/getting-started.html) or another Cloud Foundry v2 account.
* The cf gem to deploy apps on CF v2: http://docs.cloudfoundry.com/docs/dotcom/getting-started.html

## Usage

    cf push --buildpack=git://github.com/hmalphettes/heroku-buildpack-go.git

## Differences with the original buildpack

* Some bits and pieces related to python were removed.
* The '.godir' file is named '_godir': cf will omit to upload files that start with '.' by default.

Follow the PR here as we improve things: https://github.com/vito/heroku-buildpack-go/pull/1
