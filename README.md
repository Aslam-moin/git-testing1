# git-testing1
PS C:\Users\aslam\Desktop\git-testing1> git remote add upstream https://github.com/Aslam-moin/git-testing1
PS C:\Users\aslam\Desktop\git-testing1> git remore -v
git: 'remore' is not a git command. See 'git --help'.

The most similar command is
        remote
PS C:\Users\aslam\Desktop\git-testing1> git remote -v
origin  https://github.com/Aslam-Moinuddin/git-testing1.git (fetch)
origin  https://github.com/Aslam-Moinuddin/git-testing1.git (push)
upstream        https://github.com/Aslam-moin/git-testing1 (fetch)
upstream        https://github.com/Aslam-moin/git-testing1 (push)
PS C:\Users\aslam\Desktop\git-testing1> git branch develop
PS C:\Users\aslam\Desktop\git-testing1> git checkout develop 
Switched to branch 'develop'
PS C:\Users\aslam\Desktop\git-testing1> git pull upstream/main
fatal: 'upstream/main' does not appear to be a git repository
fatal: Could not read from remote repository.

Please make sure you have the correct access rights
and the repository exists.
PS C:\Users\aslam\Desktop\git-testing1> git pull upstream main
From https://github.com/Aslam-moin/git-testing1
 * branch            main       -> FETCH_HEAD
 * [new branch]      main       -> upstream/main
Already up to date.
PS C:\Users\aslam\Desktop\git-testing1> git log --oneline
ae0152e (HEAD -> develop, upstream/main, origin/main, origin/HEAD, main) Create README.md
PS C:\Users\aslam\Desktop\git-testing1> git status
On branch develop
nothing to commit, working tree clean
PS C:\Users\aslam\Desktop\git-testing1> git checkout -b feature/index
Switched to a new branch 'feature/index'
PS C:\Users\aslam\Desktop\git-testing1> git add .
PS C:\Users\aslam\Desktop\git-testing1> git commit -m "add index.html"
[feature/index 2c6a061] add index.html
PS C:\Users\aslam\Desktop\git-testing1> git push origin freature/index
error: src refspec freature/index does not match any
error: failed to push some refs to 'https://github.com/Aslam-Moinuddin/git-testing1.git'
PS C:\Users\aslam\Desktop\git-testing1> git branch
  develop
* feature/index
  main
PS C:\Users\aslam\Desktop\git-testing1> git push -u origin feature/index
Enumerating objects: 4, done.
Counting objects: 100% (4/4), done.
Delta compression using up to 12 threads
Compressing objects: 100% (3/3), done.
Writing objects: 100% (3/3), 429 bytes | 429.00 KiB/s, done.
Total 3 (delta 0), reused 0 (delta 0), pack-reused 0 (from 0)
remote: 
remote: Create a pull request for 'feature/index' on GitHub by visiting:
remote:      https://github.com/Aslam-Moinuddin/git-testing1/pull/new/feature/index
remote:
To https://github.com/Aslam-Moinuddin/git-testing1.git
 * [new branch]      feature/index -> feature/index
branch 'feature/index' set up to track 'origin/feature/index'.
PS C:\Users\aslam\Desktop\git-testing1> git checkout -b feature/style    
Switched to a new branch 'feature/style'
PS C:\Users\aslam\Desktop\git-testing1> git status
On branch feature/style
Untracked files:
  (use "git add <file>..." to include in what will be committed)
        style.css

nothing added to commit but untracked files present (use "git add" to track)
PS C:\Users\aslam\Desktop\git-testing1> git add .
PS C:\Users\aslam\Desktop\git-testing1> git commit -m "add style.css"
[feature/style dda0783] add style.css
 1 file changed, 0 insertions(+), 0 deletions(-)
 create mode 100644 style.css
PS C:\Users\aslam\Desktop\git-testing1> git push -u origin feature/style
Enumerating objects: 4, done.
Counting objects: 100% (4/4), done.
Delta compression using up to 12 threads
Compressing objects: 100% (2/2), done.
Writing objects: 100% (3/3), 313 bytes | 313.00 KiB/s, done.
Total 3 (delta 0), reused 0 (delta 0), pack-reused 0 (from 0)
remote: 
remote: Create a pull request for 'feature/style' on GitHub by visiting:
remote:      https://github.com/Aslam-Moinuddin/git-testing1/pull/new/feature/style
remote:
To https://github.com/Aslam-Moinuddin/git-testing1.git
 * [new branch]      feature/style -> feature/style
branch 'feature/style' set up to track 'origin/feature/style'.
PS C:\Users\aslam\Desktop\git-testing1> git branch
  develop
  feature/index
* feature/style
  main
PS C:\Users\aslam\Desktop\git-testing1> git checkout develop
Switched to branch 'develop'
PS C:\Users\aslam\Desktop\git-testing1> git pull origin develop
fatal: couldn't find remote ref develop
PS C:\Users\aslam\Desktop\git-testing1> git log --oneline
ae0152e (HEAD -> develop, upstream/main, origin/main, origin/HEAD, main) Create README.md
PS C:\Users\aslam\Desktop\git-testing1> git checkout feature/index
Switched to branch 'feature/index'
Your branch is up to date with 'origin/feature/index'.
PS C:\Users\aslam\Desktop\git-testing1> git log --oneline
2c6a061 (HEAD -> feature/index, origin/feature/index) add index.html
ae0152e (upstream/main, origin/main, origin/HEAD, main, develop) Create README.md
PS C:\Users\aslam\Desktop\git-testing1> git reset ae0152e
PS C:\Users\aslam\Desktop\git-testing1> git log --oneline
ae0152e (HEAD -> feature/index, upstream/main, origin/main, origin/HEAD, main, develop) Create README.md
PS C:\Users\aslam\Desktop\git-testing1> git checkout feature/style
error: The following untracked working tree files would be overwritten by checkout:
        index.html
        style.css
Please move or remove them before you switch branches.
Aborting
PS C:\Users\aslam\Desktop\git-testing1> git checkout feature/style
Switched to branch 'feature/style'
Your branch is up to date with 'origin/feature/style'.
PS C:\Users\aslam\Desktop\git-testing1> git log --oneline
dda0783 (HEAD -> feature/style, origin/feature/style) add style.css
2c6a061 (origin/feature/index) add index.html
ae0152e (upstream/main, origin/main, origin/HEAD, main, feature/index, develop) Create README.md
PS C:\Users\aslam\Desktop\git-testing1> git reset ae0152e
PS C:\Users\aslam\Desktop\git-testing1> git log --oneline
ae0152e (HEAD -> feature/style, upstream/main, origin/main, origin/HEAD, main, feature/index, develop) Create README.md
PS C:\Users\aslam\Desktop\git-testing1> git push origin main
Everything up-to-date
PS C:\Users\aslam\Desktop\git-testing1> git push origin feature/index
To https://github.com/Aslam-Moinuddin/git-testing1.git
 ! [rejected]        feature/index -> feature/index (non-fast-forward)
error: failed to push some refs to 'https://github.com/Aslam-Moinuddin/git-testing1.git'
hint: Updates were rejected because a pushed branch tip is behind its remote
hint: counterpart. If you want to integrate the remote changes, use 'git pull'
hint: before pushing again.
hint: See the 'Note about fast-forwards' in 'git push --help' for details.
PS C:\Users\aslam\Desktop\git-testing1> git push origin feature/index --force
Total 0 (delta 0), reused 0 (delta 0), pack-reused 0 (from 0)
To https://github.com/Aslam-Moinuddin/git-testing1.git
 + 2c6a061...ae0152e feature/index -> feature/index (forced update)
PS C:\Users\aslam\Desktop\git-testing1> git push origin feature/index --force
Everything up-to-date
PS C:\Users\aslam\Desktop\git-testing1> git push origin feature/style --force
Total 0 (delta 0), reused 0 (delta 0), pack-reused 0 (from 0)
To https://github.com/Aslam-Moinuddin/git-testing1.git
 + dda0783...ae0152e feature/style -> feature/style (forced update)
PS C:\Users\aslam\Desktop\git-testing1> git push -u develop
fatal: 'develop' does not appear to be a git repository
fatal: Could not read from remote repository.

Please make sure you have the correct access rights
and the repository exists.
PS C:\Users\aslam\Desktop\git-testing1> git push -u origin develop
Total 0 (delta 0), reused 0 (delta 0), pack-reused 0 (from 0)
remote: 
remote: Create a pull request for 'develop' on GitHub by visiting:
remote:      https://github.com/Aslam-Moinuddin/git-testing1/pull/new/develop
remote:
To https://github.com/Aslam-Moinuddin/git-testing1.git
 * [new branch]      develop -> develop
branch 'develop' set up to track 'origin/develop'.
PS C:\Users\aslam\Desktop\git-testing1> git branch
  develop
  feature/index
* feature/style
  main
PS C:\Users\aslam\Desktop\git-testing1> git checkout feature/index
Switched to branch 'feature/index'
Your branch is up to date with 'origin/feature/index'.
PS C:\Users\aslam\Desktop\git-testing1> git add .
PS C:\Users\aslam\Desktop\git-testing1> git commit -m "add index.html"
[feature/index ebff08f] add index.html
 1 file changed, 11 insertions(+)
 create mode 100644 index.html
PS C:\Users\aslam\Desktop\git-testing1> git push origin feature/index
Enumerating objects: 4, done.
Counting objects: 100% (4/4), done.
Delta compression using up to 12 threads
Compressing objects: 100% (3/3), done.
Writing objects: 100% (3/3), 429 bytes | 429.00 KiB/s, done.
Total 3 (delta 0), reused 0 (delta 0), pack-reused 0 (from 0)
To https://github.com/Aslam-Moinuddin/git-testing1.git
   ae0152e..ebff08f  feature/index -> feature/index
PS C:\Users\aslam\Desktop\git-testing1> git checkout feature/style
Switched to branch 'feature/style'
Your branch is up to date with 'origin/feature/style'.
PS C:\Users\aslam\Desktop\git-testing1> git pull origin feature/index
From https://github.com/Aslam-Moinuddin/git-testing1
 * branch            feature/index -> FETCH_HEAD
Updating ae0152e..ebff08f
Fast-forward
 index.html | 11 +++++++++++
 1 file changed, 11 insertions(+)
 create mode 100644 index.html
PS C:\Users\aslam\Desktop\git-testing1> git add .
PS C:\Users\aslam\Desktop\git-testing1> git commit -m "add style.css"
[feature/style 4883749] add style.css
 1 file changed, 0 insertions(+), 0 deletions(-)
 create mode 100644 style.css
PS C:\Users\aslam\Desktop\git-testing1> git push origin feature/style
Enumerating objects: 4, done.
Counting objects: 100% (4/4), done.
Delta compression using up to 12 threads
Compressing objects: 100% (2/2), done.
Writing objects: 100% (3/3), 313 bytes | 313.00 KiB/s, done.
Total 3 (delta 0), reused 0 (delta 0), pack-reused 0 (from 0)
To https://github.com/Aslam-Moinuddin/git-testing1.git
   ae0152e..4883749  feature/style -> feature/style
PS C:\Users\aslam\Desktop\git-testing1> git checkout develop
Switched to branch 'develop'
Your branch is up to date with 'origin/develop'.
PS C:\Users\aslam\Desktop\git-testing1> git pull origin develop
From https://github.com/Aslam-Moinuddin/git-testing1
 * branch            develop    -> FETCH_HEAD
Already up to date.
PS C:\Users\aslam\Desktop\git-testing1> git merge feature/index
Updating ae0152e..ebff08f
Fast-forward
 index.html | 11 +++++++++++
 1 file changed, 11 insertions(+)
 create mode 100644 index.html
PS C:\Users\aslam\Desktop\git-testing1> git merge feature/style
Updating ebff08f..4883749
Fast-forward
 style.css | 0
 1 file changed, 0 insertions(+), 0 deletions(-)
 create mode 100644 style.css
PS C:\Users\aslam\Desktop\git-testing1> git push origin develop
Total 0 (delta 0), reused 0 (delta 0), pack-reused 0 (from 0)
To https://github.com/Aslam-Moinuddin/git-testing1.git
   ae0152e..4883749  develop -> develop
PS C:\Users\aslam\Desktop\git-testing1> git log --oneline
4883749 (HEAD -> develop, origin/feature/style, origin/develop, feature/style) add style.css
ebff08f (origin/feature/index, feature/index) add index.html
ae0152e (upstream/main, origin/main, origin/HEAD, main) Create README.md
PS C:\Users\aslam\Desktop\git-testing1> git checkout develop log --oneline
error: unknown option `oneline'
usage: git checkout [<options>] <branch>
   or: git checkout [<options>] [<branch>] -- <file>...

    -b <branch>           create and checkout a new branch
    -B <branch>           create/reset and checkout a branch
    -l                    create reflog for new branch
    --[no-]guess          second guess 'git checkout <no-such-branch>' (default)
    --[no-]overlay        use overlay mode (default)
    -q, --[no-]quiet      suppress progress reporting
    --[no-]recurse-submodules[=<checkout>]
                          control recursive updating of submodules
    --[no-]progress       force progress reporting
    -m, --[no-]merge      perform a 3-way merge with the new branch
    --[no-]conflict <style>
                          conflict style (merge, diff3, or zdiff3)
    -d, --[no-]detach     detach HEAD at named commit
    -t, --[no-]track[=(direct|inherit)]
                          set branch tracking configuration
    -f, --[no-]force      force checkout (throw away local modifications)
    --[no-]orphan <new-branch>
                          new unborn branch
    --[no-]overwrite-ignore
                          update ignored files (default)
    --[no-]ignore-other-worktrees
                          do not check if another worktree is holding the given ref
    -2, --ours            checkout our version for unmerged files
    -3, --theirs          checkout their version for unmerged files
    -p, --[no-]patch      select hunks interactively
    --[no-]ignore-skip-worktree-bits
                          do not limit pathspecs to sparse entries only
    --[no-]pathspec-from-file <file>
                          read pathspec from file
    --[no-]pathspec-file-nul
                          with --pathspec-from-file, pathspec elements are separated with NUL character

PS C:\Users\aslam\Desktop\git-testing1> git checkout develop              
Already on 'develop'
Your branch is up to date with 'origin/develop'.
PS C:\Users\aslam\Desktop\git-testing1> git log --oneline
4883749 (HEAD -> develop, origin/feature/style, origin/develop, feature/style) add style.css
ebff08f (origin/feature/index, feature/index) add index.html
ae0152e (upstream/main, origin/main, origin/HEAD, main) Create README.md
PS C:\Users\aslam\Desktop\git-testing1> 