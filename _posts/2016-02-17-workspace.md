---
layout: post
title: Workspace Commands
---

<h3>Checkouts on Local Workstations</h3>

<h3><a id="designer-templates" class="anchor" href="#designer-templates" aria-hidden="true"><span aria-hidden="true" class="octicon octicon-link"></span></a>git status</h3>
<p>Shows the files or paths that have differences between the current commit and the index file, between the workspace as a whole and the index, or any path in the workspace that isn't be tracked by git.</p>

<h3><a id="designer-templates" class="anchor" href="#designer-templates" aria-hidden="true"><span aria-hidden="true" class="octicon octicon-link"></span></a>git diff [commit/branch]</h3>
<p>Shows the differences not currently in the index.  Add a specific commit or branch if the comparison should be specific.</p>

<h3><a id="designer-templates" class="anchor" href="#designer-templates" aria-hidden="true"><span aria-hidden="true" class="octicon octicon-link"></span></a>git diff --cached [commit]</h3>
<p>Displays changes staged against what has been committed.  Specific [commit] is optional; will use the latest commit if left off.</p>

<h3><a id="designer-templates" class="anchor" href="#designer-templates" aria-hidden="true"><span aria-hidden="true" class="octicon octicon-link"></span></a>git add [file/directory]</h3>
<p>Adds the specified files or directories to the index for staging into the next commit.  Can used specific filenames or wildcard with an *.  * or . can be used to add all changed files and directories.</p>

<h3><a id="designer-templates" class="anchor" href="#designer-templates" aria-hidden="true"><span aria-hidden="true" class="octicon octicon-link"></span></a>git add -u</h3>
<p>Only adds files modified to the staging area.  New files are left out.</p>

<h3><a id="designer-templates" class="anchor" href="#designer-templates" aria-hidden="true"><span aria-hidden="true" class="octicon octicon-link"></span></a>git rm file</h3>
<p>Removes the specific file from both the index and the workspace.</p>

<h3><a id="designer-templates" class="anchor" href="#designer-templates" aria-hidden="true"><span aria-hidden="true" class="octicon octicon-link"></span></a>git mv file</h3>
<p>Moves the specified file in both the index and workspace.</p>

<h3><a id="designer-templates" class="anchor" href="#designer-templates" aria-hidden="true"><span aria-hidden="true" class="octicon octicon-link"></span></a>git clean</h3>
<p>Removes all files in the current directory tree that are not being tracked.</p>

<h3><a id="designer-templates" class="anchor" href="#designer-templates" aria-hidden="true"><span aria-hidden="true" class="octicon octicon-link"></span></a>git commit -a</h3>
<p>Commits all files changed since the last commit, and deletes files removed from the workspace.</p>


<h3><a id="designer-templates" class="anchor" href="#designer-templates" aria-hidden="true"><span aria-hidden="true" class="octicon octicon-link"></span></a>git checkout [file/directory]</h3>
<p>Updates the file or directory.</p>

<h3><a id="designer-templates" class="anchor" href="#designer-templates" aria-hidden="true"><span aria-hidden="true" class="octicon octicon-link"></span></a>git checkout -- [somefilename]</h3>
<p>If unstaging isn't enough, but you want all changes on a file reverted to the last commit, use "checkout".</p>

<h3><a id="designer-templates" class="anchor" href="#designer-templates" aria-hidden="true"><span aria-hidden="true" class="octicon octicon-link"></span></a>git reset [somefilename]</h3>
<p>If you decide to not commit a change, use this command to unstage a change.</p>

<h3><a id="designer-templates" class="anchor" href="#designer-templates" aria-hidden="true"><span aria-hidden="true" class="octicon octicon-link"></span></a>git reset --hard</h3>
<p>All files changed since last commit are lost and workspace reverts to the local tree. Recommndations are to only use if a merge has caused an insurmountable conflict.</p>

<h3><a id="designer-templates" class="anchor" href="#designer-templates" aria-hidden="true"><span aria-hidden="true" class="octicon octicon-link"></span></a>git reset --hard origin/master</h3>
<p>All files changed since last commit on the local repository are lost, and now match the remote/branch.  Origin/master are used here because those are typical names.</p>

<h3><a id="designer-templates" class="anchor" href="#designer-templates" aria-hidden="true"><span aria-hidden="true" class="octicon octicon-link"></span></a>git reset HEAD [file]</h3>
<p>Removes file typed in from being included in the next commit.  The changes are still available, but not included in the next commit.</p>

<h3><a id="designer-templates" class="anchor" href="#designer-templates" aria-hidden="true"><span aria-hidden="true" class="octicon octicon-link"></span></a>git reset --soft HEAD^</h3>
<p>Removes the last commit, but the changes are kept.

<h3><a id="designer-templates" class="anchor" href="#designer-templates" aria-hidden="true"><span aria-hidden="true" class="octicon octicon-link"></span></a>git checkout [newbranch]</h3>
<p>Switch to the new branch.</p>

<h3><a id="designer-templates" class="anchor" href="#designer-templates" aria-hidden="true"><span aria-hidden="true" class="octicon octicon-link"></span></a>git checkout -b [newbranch]</h3>
<p>Create new branch and switch to it at the same time.</p>

<h3><a id="designer-templates" class="anchor" href="#designer-templates" aria-hidden="true"><span aria-hidden="true" class="octicon octicon-link"></span></a>git merge [branch]</h3>
<p>Merge your changes from a dev branch into the master or current branch.</p>

<h3><a id="designer-templates" class="anchor" href="#designer-templates" aria-hidden="true"><span aria-hidden="true" class="octicon octicon-link"></span></a>git rebase upstream</h3>
<p>Reverts all commits from the time the branch diverged.</p>

<h3><a id="designer-templates" class="anchor" href="#designer-templates" aria-hidden="true"><span aria-hidden="true" class="octicon octicon-link"></span></a>git cherry-pick [commit]</h3>
<p>Installs changes for the selected [commit] into the current branch.</p>

<h3><a id="designer-templates" class="anchor" href="#designer-templates" aria-hidden="true"><span aria-hidden="true" class="octicon octicon-link"></span></a>git revert [commit]</h3>
<p>Reversese any change made at the selected [commit] and then commits the result.</p>

<h3><a id="designer-templates" class="anchor" href="#designer-templates" aria-hidden="true"><span aria-hidden="true" class="octicon octicon-link"></span></a>git clone [repo]</h3>
<p>Downloads the specified repo to the local workarea and creates a checkout of the master.  <repo> is typically a remote like https://github.com/[username]/[yourrepo].git, but it can also be a local repository.</p>

<h3><a id="designer-templates" class="anchor" href="#designer-templates" aria-hidden="true"><span aria-hidden="true" class="octicon octicon-link"></span></a>git pull origin master</h3>
<p>Pulls code from your "origin" remote, master and pulls changes into the local.  Useful if code in your local repository is not as current as, say, the GitHub code.</p>