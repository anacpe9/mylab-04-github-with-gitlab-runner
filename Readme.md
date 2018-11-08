# Using GitLab CI/CD with a GitHub repository

---

## Objective

- can use CI/CD with github.com

## Steps

### Github setting up

#### [Integrate your server with GitHub](https://docs.gitlab.com/ee/integration/github.html)

- [generation new github 'personal access token' with `repo` and `admin:repo_hook` scope](https://github.com/settings/tokens/new)
  - [url to generate 'personal access token'](https://github.com/settings/tokens/new)
  - At least, The `repo` and `admin:repo_hook` should be enable to allow GitLab access
  - ***Important*** copy & save
  - `***`

### Gitlab setting up

#### [Using GitLab CI/CD with a GitHub repository](https://docs.gitlab.com/ee/ci/ci_cd_for_external_repos/github_integration.html)

- [<project>/Settings/Repository/<Mirror a repository>](https://docs.gitlab.com/ee/workflow/repository_mirroring.html#pulling-from-a-remote-repository)
- [<project>/Settings/Integrations/<Github>](https://docs.gitlab.com/ee/ci/ci_cd_for_external_repos/github_integration.html)
  - see **Connect manually** section
  - [generation new gitlab 'personal access token' with `api` scope](Personal Access Token)
  - [GitHub project integration](https://docs.gitlab.com/ee/user/project/integrations/github.html)
    - ***Important*** must check `Trigger pipelines for mirror updates`, when add `Mirror a repository`
    - ****OR*** use webhook [Triggering pipelines through the API](https://docs.gitlab.com/ee/ci/triggers/)
  - **Github** `Setting > Webhooks` - `https://gitlab.com/api/v4/projects/<NAMESPACE>%2F<PROJECT>/mirror/pull?private_token=<PERSONAL_ACCESS_TOKEN>`
  - ***OR*** Github `Setting > Webhooks` - `https://gitlab.example.com/api/v4/projects/:<Project ID>/mirror/pull?private_token=<PERSONAL_ACCESS_TOKEN>`
    - [Start the pull mirroring process for a Project: API](https://docs.gitlab.com/ee/api/projects.html#start-the-pull-mirroring-process-for-a-project-starter)
