# Obdi

## Screenshot

![](images/screenshot-2014-10.27.png?raw=true)

## What is it?

Obdi is an extendable graphical user interface for running scripts on
remote servers.  The most basic installation provides administrative tools to
manage users, data centres and environments, and includes a job manager.

## Status

Development and testing phase. Not ready for use.

## Features

* All GUI items in the screen shot are implemented using plugins.
* Plugins can be REST end-points - they can be used for automation.
* The saltconfigserver plugin contains a number of REST end-points, including an External Node Classifier (ENC).

## Architecture

* Google Go for the back end REST interface.
* Angular JS and bootstrap for the front end.
* Sqlite3 used for data storage.
* Obdi simply runs scripts on remote servers, so it can be used for lots of different tasks.

## Install

This package is "go-gettable", but will require a lot of moving things around to get working.

```
go get github.com/mclarkson/obdi
```
For Red Hat based systems RPMs can be built using:
```
cd
yum install rpmdevtools gcc
git clone https://github.com/mclarkson/obdi.git
cd fdp-mgmt-obdi
BUILD_NUMBER=1 ./dist/jenkins-build.sh
```

## Todo

Front-end

* Versioning plugin
* Key Management plugin
* Salt job viewer plugin
* Scripting plugin (chainable)
* System Log plugin
* Monitoring plugin

Back-end

* Expose system log so plugins can use it.

