# Maven Scripts

## SonarQube Project Scan

If you want to use SonarQube to scan your application code import this script to your **.gitlab-ci.yml**.

```yaml
include:
  - remote: 'https://raw.githubusercontent.com/nikolicjakov/gitlab-ci-scripts/master/maven/maven_sonar.yml'
```

This script expects that your have project CI environment variables set in your GitLab project configuration.

 - SONAR_HOST = URL address of your SonarQube instance.
 - SONAR_TOKEN = Sonar token used to publish analysis results. (Generated on SonarQube server.)
 - SONAR_ARGS = All additional arguments that you would like to pass in sonar execution.