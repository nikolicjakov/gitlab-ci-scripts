# GitLab CI Scripts

![GitLab CI Scripts](resources/img/gitlabci-bckg.png)

__*This project aims to centralize gitlab pipeline configuration. In this project we hold generic reusable pipeline scripts for different kind of tasks (build, test, deploy).*__

---

## Project structure.

Code in this project is organized by folders that match tool or purpose of the script itself. By looking at folder names you are able to find scripts needed.

## How to include script in your project?

To include script in your project you need to update gitlab pipeline file named **_.gitlab-ci.yml_** in your project root directory.
If you dont have such file you should create one in root directory of your project.
This example is showing how you can include scripts from this repository to your project pipeline.

```yaml
include:
  - remote: 'https://raw.githubusercontent.com/nikolicjakov/gitlab-ci-scripts/master/docker/kaniko_build.yml'
```
This will add kaniko docker build script to __package__ stage of project pipeline.

You are also able to include multiple scripts, listing them all one by one as shown in this example.

```yaml
include:
  - remote: 'https://raw.githubusercontent.com/nikolicjakov/gitlab-ci-scripts/master/script-1.yml'
  - remote: 'https://raw.githubusercontent.com/nikolicjakov/gitlab-ci-scripts/master/script-2.yml'
  - remote: 'https://raw.githubusercontent.com/nikolicjakov/gitlab-ci-scripts/master/script-3.yml'
```