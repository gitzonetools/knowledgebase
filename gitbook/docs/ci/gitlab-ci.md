# Gitlab CI
Gitlab CI is a Continuous Integration service developed and maintained by GitLab Inc. It is available for free as Open Source to self install. As of now the on demand service at gitlab.com is also free to use.
This doc covers the software.

## Positive
1. Scale automatically on demand
1. Runs entirely in docker
1. You can do about anything, just output exit code 0 or 1 at the end to indicate success or failure

## Negative
1. Basically none

## How we approach it at Lossless
1. We wrote a library called [npmci](https://gitzone.gitlab.io/npmci)

## Watch and Learn

## Links to learn more
* http://doc.gitlab.com/ee/ci/yaml/README.html
* https://gitlab.com/gitlab-org/gitlab-ci-multi-runner
* http://stackoverflow.com/questions/20424814/are-gitlab-deployment-keys-read-only

To see/edit the config use the following command:

```sh
sudo nano /etc/gitlab-runner/config.toml
```
