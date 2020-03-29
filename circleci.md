## Category

### What is difference between job and workspace?
If you are not using workflows, the jobs map must contain a job named build.
This build job is the default entry-point for a run that is triggered by a push to your VCS provider.
It is possible to then specify additional jobs and run them using the CircleCI API.
- https://circleci.com/docs/2.0/configuration-reference/#jobs
- https://circleci.com/docs/2.0/configuration-reference/#workflows
- https://circleci.com/docs/2.0/workflows/
- https://circleci.com/blog/modernizing-federal-devops-circleci-becomes-first-continuous-integration-tool-with-fedramp-authorization/
- https://circleci.com/docs/2.0/jobs-steps/

### What is orbs?
```
version: 2.1

orbs:
  maven: circleci/maven@0.0.12

workflows:
  maven_test:
    jobs:
      - maven/test # checkout, build, test, and upload test results
```
- https://circleci.com/orbs/
- https://circleci.com/orbs/registry/orb/circleci/maven

### Do jobs also run when workflows are defined?
No, workflows run only. If you are not using workflows, the jobs map must contain a job named build. This build job is the default entry-point for a run that is triggered by a push to your VCS provider.

### How do I find pre-built docker images?
- https://circleci.com/docs/2.0/circleci-images/#image-types

### How do I find configuration keys?
- https://circleci.com/docs/2.0/configuration-reference/#steps
- Check out source code: https://circleci.com/docs/2.0/configuration-reference/#checkout
- Restores a previously saved cache: https://circleci.com/docs/2.0/configuration-reference/#restore_cache
- Persist a temporary file to be used by another job in the workflow: https://circleci.com/docs/2.0/configuration-reference/#persist_to_workspace
- Generates and stores a cache of a file or directory of files such as dependencies or source code in our object storage: https://circleci.com/docs/2.0/configuration-reference/#save_cache
- Attach the workflow’s workspace to the current container: https://circleci.com/docs/2.0/configuration-reference/#attach_workspace
- Upload and store test results for a build. Test results are visible on the CircleCI web application, under each build's "Test Summary" section: https://circleci.com/docs/2.0/configuration-reference/#store_test_results
- Store artifacts (for example logs, binaries, etc) to be available in the web app or through the API: https://circleci.com/docs/2.0/configuration-reference/#store_artifacts
- Used for orchestrating all jobs: https://circleci.com/docs/2.0/configuration-reference/#workflows
- Defines rules for allowing/blocking execution of some branches: https://circleci.com/docs/2.0/configuration-reference/#branches
- Execute Workflows for a Git Tag: https://circleci.com/docs/2.0/configuration-reference/#tags
  - https://circleci.com/docs/2.0/workflows/#executing-workflows-for-a-git-tag
  - Semantic Versioning: https://semver.org/ and https://en.wikipedia.org/wiki/Software_versioning
