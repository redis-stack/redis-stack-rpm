# redis-stack-rpm

This repository takes the promoted [redis-stack](https://github.com/redis-stack/redis-stack) rpm, updates a YUM repository, and uploads the artifacts to S3.

Publishing RPMs involve:

1. Publishing a release using the release tool in [redis-stack](https://github.com/redis-stack/redis-stack).
2. Waiting for the [publish release](https://github.com/redis-stack/redis-stack/actions/workflows/release.yml) action to complete, promoting the releases.
3. Tagging this repository, with the same tag created in redis-stack.

Note: until this repository changes to use rpm-s3, it cannot support multiple releases (i.e parallel releases) at the same time.
