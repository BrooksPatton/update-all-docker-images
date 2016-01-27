# update-all-docker-images
A bash script to update all docker images installed on the computer

## Usage
<code>./docker-images-update.sh</code>

## What will this do

This script will go through all of your docker images and pull the latest versions of them from docker hub, or whatever repository you have docker set to.

This is important to do as security updates can be pushed out to images, including tags for older versions. This way you will always get the latest and greatest when you work with docker.

## Files Created

A error file is created by this script if there is an error from the docker pull command. This error will be placed into the **/tmp/docker-images-update.error** file by default. If you would like it to be changed, then change the **ERROR_FILE** variable in the script before running.

## What about docker images not in a repository?

They will cause an error when docker attempts to update them. This script checks the error message and skips over these images.
