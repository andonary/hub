## Objective

!!! error "This job is deprecated 🚨"
    The job is no more maintained and is now deprecated. Despites it still exists to keep working on pipelines.

Tox aims to automate and standardize testing in Python. It is part of a larger vision of easing the packaging, testing and release process of Python software.

## How to use it

1. Ensure that your project have
   [`tox.ini`](https://tox.wiki/en/latest/){:target="_blank"}
   file
1. Copy/paste job URL in `include` list of your `.gitlab-ci.yml` (see the [quick use](https://docs.r2devops.io/get-started/use-templates/#use-a-template)). You can specify [a fixed version](https://docs.r2devops.io/get-started/use-templates/#versioning) instead of `latest`.
1. If you need to customize the job (stage, variables, ...) 👉 check the [jobs
   customization](https://docs.r2devops.io/get-started/use-templates/#job-templates-customization)
1. Well done, your job is ready to work ! 😀

## Variables

| Name | Description | Default |
| ---- | ----------- | ------- |
| `PROJECT_ROOT` <img width=100/> | Relative to root of your repository, it is the path to your python project <img width=175/>| `.` <img width=100/>|
| `PYTHON_ENV` | Restrict the test to run on a specific environment of Python, if none is specified `Tox` will run the test on all environment listed in the `tox.ini` file. | ` ` |
| `ADDITIONAL_OPTIONS` | [Additional options](https://tox.wiki/en/latest/config.html?result-json#tox) for tox command | ` ` |
| `IMAGE_TAG` | The default tag for the docker image | `slim-focal`  |



## Author
This resource is an **[official job](https://docs.r2devops.io/get-started/faq/#use-a-template)** added in [**R2Devops repository**](https://gitlab.com/r2devops/hub) by [@alexiaognard](https://gitlab.com/alexiaognard)
