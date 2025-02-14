# Docker Hub

Source behind the following images:

- https://hub.docker.com/_/composer (official) 
- https://hub.docker.com/r/composer/composer (community)

Docker Hub documentation can be found at https://github.com/docker-library/docs/tree/master/composer


## Official Image

The official image release workflow is as follows:

- :robot: a new tag is pushed to [Composer repository]
- :robot: [release workflow] on [Composer repository] creates an issue regarding new tag on [Docker repository]
- :writing_hand: modification to relevant `Dockerfile`s is pushed/merged
- :writing_hand: a pull request is submitted to the [official images repository]
- :writing_hand: pull request is merged, resulting in new release being added to [Docker Hub](https://hub.docker.com/_/composer)


## Community Image

The community image release workflow is as follows:

- :robot: a new tag is pushed to [Composer repository]
- :robot: [release workflow] on [Composer repository] creates an issue regarding new tag on [Docker repository]
- :writing_hand: modification to relevant `Dockerfile`s is pushed/merged
- :robot: [docker workflow] builds and pushes new release to [Docker Hub](https://hub.docker.com/r/composer/composer)


[composer repository]: https://github.com/composer/composer
[docker repository]: https://github.com/composer/docker
[official images repository]: https://github.com/docker-library/official-images/
[release workflow]: https://github.com/composer/composer/blob/832af78e284b23a8f43914b2571fb4c48a7b108a/.github/workflows/release.yml#L81-L96
[docker workflow]: https://github.com/composer/docker/blob/master/.github/workflows/docker.yaml
