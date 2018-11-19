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

*****************************

current version: 0.1.0-unstable.0
change env: DEV
action: dummy change
after commit+push version: 0.1.0-unstable.1

*****************************

current version: 0.1.0-unstable.1
change env: DEV
action: dummy change
after commit+push version: 0.1.0-unstable.2

*****************************

current version: 0.1.0-unstable.2
env: branch "develop" to "release/0.1.0-rc.1"
action:

mode: ContinuousDeployment
ignore:
  sha: []
branches:
  develop:
    mode: ContinuousDeployment
    tag: unstable
    increment: Patch
  releases?[/-]:
    mode: ContinuousDelivery
    tag: rc
    increment: Patch
    prevent-increment-of-merged-branch-version: true

after commit+push version: 0.1.0-rc1+3

*****************************

current version: 0.1.0-rc1+3
env: release/0.1.0-rc.1
action: dummy change
after commit+push version: 0.1.0-rc.1+4

wswwssw
aaaswswsss
s

aa

sssswswswsw
sdfjsfdhjfdhaaa