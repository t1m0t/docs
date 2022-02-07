# Presentation

This repository contains the documentation of Dioxus repository only.
It is organised in a way that each branch relates to a release version.
When a new release is published, the next branch will become a new branch named with the new release version.

# Process

When new release is published, we would do:
 - `git branch new_version_released`
 - `git checkout new_version_released`
 - `git rebase next new_version_released`

# Doc updates

The idea is to not update published release branches (`v0.1.8` for instance) except when there is a typo or something important that was missing and need to be updated.
We should update like this:
 1. New docs to commit to `master` branch
 2. When new docs confirmed to be published, rebase `master` branch to `next`: `git rebase master next`
 3. When new release published, rebase `next` branch to `new_version_released`: `git rebase next new_version_released`