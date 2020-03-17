## Category

### What is different between job and workspace?
If you are not using workflows, the jobs map must contain a job named build.
This build job is the default entry-point for a run that is triggered by a push to your VCS provider.
It is possible to then specify additional jobs and run them using the CircleCI API.
- https://circleci.com/docs/2.0/configuration-reference/#jobs
- https://circleci.com/docs/2.0/configuration-reference/#workflows
- https://circleci.com/docs/2.0/workflows/
- https://circleci.com/blog/modernizing-federal-devops-circleci-becomes-first-continuous-integration-tool-with-fedramp-authorization/
- https://circleci.com/docs/2.0/jobs-steps/
