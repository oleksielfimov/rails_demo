# Engine Yard Cloud Quick Deploy #

This is a bash script for doing super quick deploys on Engine Yard Cloud. Perfect for when you just need to fix a quick typo. Deploys quick changes to a single app server in typically <~2s.

## Install ##

Run this:

    mkdir -p ~/bin && curl https://raw.github.com/gist/1872050/086475dcbc8e7d92d55ce0757d3692d77793f4b1/ey_deploy.sh > ~/bin/ey_deploy && chmod +x ~/bin/ey_deploy

Then create a .ey file in your project root directory. See .ey-example

## How to use it ##

Deploy changes (using rsync):

    ey_deploy

Deploy changes with migrations:

    ey_deploy -m

Deploy changes and run asset precompilation:

    ey_deploy -p

Deploy changes and clear the page cache:

    ey_deploy -c

## What does it do? ##

All this does is rsyncs your local code to your Engine Yard Cloud servers. It doesn't do any sanity checks or anything, so you'll still want to run `ey deploy` once in a while. But for day to day deploying, you won't get much faster than this.