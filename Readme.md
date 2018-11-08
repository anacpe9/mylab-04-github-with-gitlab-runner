# Using GitLab CI/CD with a GitHub repository

---

## Objective

- can use CI/CD with github.com

## Steps

### Github setting up

#### [Integrate your server with GitHub](https://docs.gitlab.com/ee/integration/github.html)

- [generation new github 'personal access token'](https://github.com/settings/tokens/new)
  - [url to generate token](https://github.com/settings/tokens/new)
  - At least, The `repo` and `admin:repo_hook` should be enable to allow GitLab access
  - ***Important*** copy & save
  - `***`

### Gitlab setting up

#### [Using GitLab CI/CD with a GitHub repository](https://docs.gitlab.com/ee/ci/ci_cd_for_external_repos/github_integration.html)

- [<project>/Settings/Repository/<Mirror a repository>](https://docs.gitlab.com/ee/workflow/repository_mirroring.html#pulling-from-a-remote-repository)
- [<project>/Settings/Integrations/<Github>](https://docs.gitlab.com/ee/ci/ci_cd_for_external_repos/github_integration.html)
