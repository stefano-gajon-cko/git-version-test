# git-version-test
just few test for got versioning

initial configuration:

mode: ContinuousDeployment
ignore:
  sha: []
branches:
  develop:
    mode: ContinuousDeployment
    tag: unstable
    increment: Patch
  release:
    mode: ContinuousDelivery
    tag: rc
    increment: Patch
    prevent-increment-of-merged-branch-version: true



current version: 0.1.0-unstable.0
change env: DEV
action: dummy change