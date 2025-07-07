# Argo Workflows

This folder contains workflows that are used for automation and one-off tasks.

The structure is as follows:

* `once` is the folder that contains one-off workflows. These should **not** be auto-deployed and
  can be copy/pasted into Argo to execute. They're stored here as a record of what was done.
* `templates` are workflow templates, which are then used to run ad-hoc work using the UI
  or scheduled work using a `cron` workflow.
* `cron` is the folder full of scheduled tasks. These run a parameterised `template` and should
  alert someone if they fail.

## Hints and tips

Don't forget to add your workflow template or cron job to the `kustomize.yaml` file in the
folder you put it in!
