+++
date = "2015-12-05T16:00:21-08:00"
draft = false
title = "Bitbucket Cloud"
weight = 24
menu = "installation"
toc = true
+++

# Overview

Drone comes with built-in support for Bitbucket Cloud. To enable Bitbucket Cloud you should configure the driver using the following environment variables:

```bash
BITBUCKET_CLIENT=...
BITBUCKET_SECRET=...
```

# Configuration

This is a full list of configuration options. Please note that many of these options use default configuration value that should work for the majority of installations.

NAME                        | DESC
----------------------------|--------------------------------------------------------
`DRONE_STASH_CONSUMER_KEY`  | bitbucket consumer key
`DRONE_STASH_CONSUMER_RSA`  | bitbucket consumer secret


# Registration

You must register your application with Bitbucket in order to generate a Client and Secret. Navigate to your account settings and choose OAuth from the menu, and click Add Consumer.

Please use `http://drone.mycompany.com/authorize` as the Authorization callback URL. You will also need to check the following permissions:

* Account:Email
* Account:Read
* Team Membership:Read
* Repositories:Read
* Webhooks:Read and Write

# Missing Features

Please note that Drone does not currently support the features listed below. We are absolutely open to pull requests to include this functionality. If you are interested in contributing to Drone and adding these capabilities please [get in touch](https://gitter.im/drone/drone).

* Merge request events are not supported due to lack of merge ref
* Mercurial repositories are not supported out-of-the box