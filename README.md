# learning-ruby

I don't know all that much ruby (specifically rails). Lets change that.

## What is this?

This is a useless API that I created specifically for learning Ruby and Ruby on Rails. Please do not use this as any sort of example, there are probably lots of things I did incorrectly here. Also and this should go without saying, please don't try to use this in production.

## The plan

The plan is to create an API that consumes the HackerNews API and then spits out result formatted in some way (did I mention this thing was useless?). From there attach all the necessary things that a production API will require in the real world, linting, tests, etc.

## Setup

1. Install RVM ([link](https://rvm.io))

## Build Log

Just a little log of my journey

**Monday April 13, 2020**: The setup. So far everything is going smoothly. Had to make a decision right off the bat whether I wanted to use a regular installation or Ruby, RVM or RBENV. Decided to go with RVM for the time being though I don't think that has a bearing on future work and can be swapped out easily. Reading up on how .rvmrc and .ruby_version configuration files work. Seemed like rvmrc was the way to go but after reading about some of the limitations, using .ruby_version should suffice.

Overall there is a ton of learning at this stage. While I've always worked on Ruby project in the past, I've never had that great of an idea about how they are boilerplated. Also I just realized I misconfigured RVM which was causing issues with sudo and root. I thought this was a bit quirky at first but after reading some more into it, it seems that I forgot to log out after installing RVM so my user never got added to the `rvm` group in Ubuntu, hence permissions errors.

Well it seems that the `rails new` by itself may be a little to heavy handed. When I first created a project using `rails new .`, it created a base rails setup but also added in a bunch of other packages. I get why they do this to showoff what the framework can do, but I'll be consulting with `--help` to see if there is a better way of generating a smaller initial project without some of the extras. And after no more than a few seconds of digging I found the flag I was looking for: `--api`. This will create a slimmed down rails project strictly for API based apps. While I may revisit the topic of running a full fledged site with Ruby, for now I'm learning primarily the Rails API side so I will be sticking to that.
