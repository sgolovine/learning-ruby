# learning-ruby

I don't know all that much ruby (specifically rails). Lets change that.

## What is this?

This is a useless API that I created specifically for learning Ruby and Ruby on Rails. Please do not use this as any sort of example, there are probably lots of things I did incorrectly here. Also and this should go without saying, please don't try to use this in production.

## The plan

The plan is to create an API that consumes the HackerNews API and then spits out result formatted in some way (did I mention this thing was useless?). From there attach all the necessary things that a production API will require in the real world, linting, tests, etc.

## Setup

1. Install RVM ([link](https://rvm.io))
2. Once installed make sure you are running the right version of Ruby (check `.ruby-version`)
3. `bundle install`

## Running the API

WIP

## Build Log

Just a little log of my journey

**Monday April 13, 2020**: The setup. So far everything is going smoothly. Had to make a decision right off the bat whether I wanted to use a regular installation or Ruby, RVM or RBENV. Decided to go with RVM for the time being though I don't think that has a bearing on future work and can be swapped out easily. Reading up on how .rvmrc and .ruby_version configuration files work. Seemed like rvmrc was the way to go but after reading about some of the limitations, using .ruby_version should suffice.

Overall there is a ton of learning at this stage. While I've always worked on Ruby project in the past, I've never had that great of an idea about how they are boilerplated. Also I just realized I misconfigured RVM which was causing issues with sudo and root. I thought this was a bit quirky at first but after reading some more into it, it seems that I forgot to log out after installing RVM so my user never got added to the `rvm` group in Ubuntu, hence permissions errors.

Well it seems that the `rails new` by itself may be a little to heavy handed. When I first created a project using `rails new .`, it created a rails setup for a full fledged app. This is a bit too much for my scope as I want to focus on the backend side of things (where Rails is used the most) so I opted to re-create the rails setup using the `--api` flag which doesn't add any extra packages required for a full fledged webapp.
