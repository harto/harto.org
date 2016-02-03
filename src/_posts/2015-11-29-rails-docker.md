---
layout: post
title: Setting up a Rails app for Docker development on OS X
---

see also https://robots.thoughtbot.com/rails-on-docker

 - homebrew
 - brew install docker
 - brew install docker-compose?
 - brew install docker-machine?
 - docker-machine create --driver=virtualbox development
 - eval "$(docker-machine env development)"
 - docker-compose.yml
   - need to figure out gem volume mounting
 - docker-compose run web bash
 - bundle install rails
 - rails new --skip-javascript --skip-sprockets --... <name>
 -
