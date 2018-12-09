# Gulp
Gulp is an awesome streaming build system built on nodejs. It utilizes node streams to deal with files in chunks. (Every file is one chunk).

## Positive:
1. A standard way of doing things
1. Wide support by the community
1. Easy to write and expandable
1. Considerably easy on memory when handling thousands of files, since files move trough the pipeline at a complete maximum of 16 at one time. Only when a file/chunk leaves the pipeline a new one is picked up.  


## Negative:
1. Tool sometimes seems stuck with an old inefiicient dependency tree
1. Too much boilerplate: We usually like it maintainable and good by convention over configuration

## Our approach at Lossless
1. We wrote a really lightweight gulp replacement called [smartgulp](https://pushrocks.gitlab.io/smartgulp)
1. We compose streams with our own [smartstream](https://pushrocks.gitlab.io/smartstream) that handles errors with feedback like a champ
1. We take the pain out of plugins with our [gulp-function](https://pushrocks.gitlab.io/gulp-function) plugins: With support for promises.

## Watch and learn


## Links to learn more
