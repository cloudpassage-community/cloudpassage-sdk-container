# CloudPassage SDK

## This repo is used for automated builds of the CloudPassage SDK container image.

The image tags indicate the base image and the version of the SDK included in the image, and may include a date to enable more precise pinning.

This is how to understand the SDK container image tagging scheme:

Consider this image: halotools/python-sdk:ubuntu-16.04_sdk-1.0.4_2017-12-31

We can infer from the tag that this image is based on Ubuntu 16, includes
version 1.0.4 of the SDK, and was built on the last day of December, 2017.

These images only include Python 2.7 and pip.  Git is not included. If you have
git repositories that you need to clone into the container, we encourage you
to use [multi-stage builds](https://docs.docker.com/engine/userguide/eng-image/multistage-build/)
to keep your resulting image as small as possible, and avoid including
unnecessary components.
