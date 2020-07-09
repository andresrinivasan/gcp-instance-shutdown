# GCP Instance Shutdown

A simple Google Cloud Function that when invoked either loops through named instances and/or running instances with a particular label and shuts them down.

## Why

I was forgetting to shutdown my GCP instances at night and when I searched for a way to automate the process I came across [Using Pub/Sub to trigger a Cloud Function](https://cloud.google.com/scheduler/docs/tut-pub-sub). But the cloud function is written in Node.js and there was no Go equivalent (that I could find). It must be written.

## What

The cloud function listens on a pub/sub topic and expects a list of named instances and/or a list of labels. In the case of named instances, the function attempts to stop each one. For the labels, running instances are filtered based on the labels. For each resulting instance the function attempts to stop it.

## Install

## Configure
