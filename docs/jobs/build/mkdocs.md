# 📃 Mkdocs

## Description

Build HTML documentation form Markdown source using
[Mkdocs](https://www.mkdocs.org/). All requirements to use [Material for
Mkdocs](https://squidfunk.github.io/mkdocs-material/) are ready to use.

## How to use it

1. Prepare your project with Mkdocs configuration file and sources files as
   described in [Mkdocs
   documentation](https://www.mkdocs.org/#getting-started). In your repository,
   documentation files must be organized as follows:

    ```
    /mkdocs.yml # This is your configuration file
    /docs/      # This folder contains all your documentation markdown files
    ```
2. Add the corresponding URL to your `.gitlab-ci.yml` file (see [Getting
   started](/getting-started)). You can use a specific version from [version
   list](#versions). Example with default (`latest`):

    ```yaml
    include:
      - remote: 'https://jobs.go2scale.io/mkdocs.yml'
    ```
3. If you need set variables, see [Jobs
   customization](/getting-started#jobs-customization) section in
   getting started

## Jobs

### Documentation

Build HTML documentation from Makdown source using `Mkdocs`.

* Docker image:
[squidfunk/mkdocs-material](https://hub.docker.com/r/squidfunk/mkdocs-material)
* When: always
* Stage: build
* Artifacts:
    * Result of documentation build exposed as `Documentation`
* Variables:

| Name | Description | Default |
| ---- | ----------- | ------- |
| `DOCUMENTATION_DISABLE` | Disable build | |


## Versions

* **Latest** : `https://jobs.go2scale.io/latest/mkdocs.yml`
* **Tag `2020-07-15_1`** : `https://jobs.go2scale.io/2020-07-15_1/mkdocs.yml`

    !!! warning
        Since this version, `pages` job, which publish documentation on Gitlab
        pages, isn't included anymore. It's now a dedicated job:
        [pages](Jobs/pages).

* **Tag `2020-05-31_1`** (legacy): `https://gitlab.com/go2scale/hub/-/raw/2020-05-31_1/jobs/documentation.gitlab-ci.yml`

    !!! warning
        This update introduces breaking changes. Follow [this
        guide](https://squidfunk.github.io/mkdocs-material/releases/5/#how-to-upgrade)
        to know how to upgrade.
    * Upgrade Material for Mkdocs to v5

* **Tag `2020-05-31_1`** (legacy): `https://gitlab.com/go2scale/hub/-/raw/2020-05-05_3/jobs/documentation.gitlab-ci.yml`

    * Initial version