# Shared Runner for Gitlab

## Summary
This repo builds a shared-runner. The runner has been created with an autoscaling group that allow for scale-in and scale-out; there are also scheduled tasks to tear down the runners and rebuild them with updates for OS and Gitlab runner software.

## Overall process
1.  Create a branch for your changes
2.  For a new runner, copy the .template to a new file for your new runner
3.  In the user data section of the template, pay attention to the gitlab-runner commands for editing the type of executor, token for registration, and descriptions of the runner
4.  For changes to existing runners, make changes to the template file 

## Process to change a runner
1. `git checkout -b *name of your branch*`
2. Make changes to the template and save the template file
3. Create a merge request with details of the reason for the change - especially if this is a permission change

## Process to create a runner
1. `git checkout -b *name of your branch*`
2. Make changes to the template and save the template file and save the template and parameters (.json) files to the name of your runner
3. Create a merge request with details of the new runner