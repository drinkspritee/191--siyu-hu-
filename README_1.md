Last login: Fri Jan 24 21:05:42 on ttys006

The default interactive shell is now zsh.
To update your account to use zsh, please run `chsh -s /bin/zsh`.
For more details, please visit https://support.apple.com/kb/HT208050.
Janes-MBP:basic-commits siyuhu$ git status
On branch master
Your branch is ahead of 'origin/master' by 1 commit.
  (use "git push" to publish your local commits)

Untracked files:
  (use "git add <file>..." to include in what will be committed)

	../3-way-merge/.Rhistory

nothing added to commit but untracked files present (use "git add" to track)
Janes-MBP:basic-commits siyuhu$ git log
commit 8ebb496b076bd1b899c00ed305ac860a65113139 (HEAD -> master, greeting)
Author: drinkspritee <siyuh4@uci.edu>
Date:   Fri Jan 24 19:18:14 2020 -0800

    Add greeting

commit f8712d5c4df74fa0d49c8cc9ba3b1a5b2c571072 (origin/master, origin/HEAD)
Author: Frank Theile <ftheile@grundfos.com>
Date:   Mon Dec 9 10:30:13 2019 +0100

    Add missing shebang in squashing/setup.sh
    
    `setup.sh` should be executable according to the instructions given in README.md

commit e060df632bf4799da9aa1c0092640563acf84588
Author: Adam Matan <adamatan@users.noreply.github.com>
Date:   Wed Dec 4 07:46:31 2019 +0200

    Word ordering

commit 6ccb85882dc12fb0b26acd65bead2fc7da57a187
Author: Frank Theile <ftheile@grundfos.com>

[1]+  Stopped                 git log
Janes-MBP:basic-commits siyuhu$ git add example.txt
fatal: pathspec 'example.txt' did not match any files
Janes-MBP:basic-commits siyuhu$ cd katas
-bash: cd: katas: No such file or directory
Janes-MBP:basic-commits siyuhu$ touch example.txt
Janes-MBP:basic-commits siyuhu$ git status
On branch master
Your branch is ahead of 'origin/master' by 1 commit.
  (use "git push" to publish your local commits)

Untracked files:
  (use "git add <file>..." to include in what will be committed)

	../3-way-merge/.Rhistory
	example.txt

nothing added to commit but untracked files present (use "git add" to track)
Janes-MBP:basic-commits siyuhu$ .setup.sh
-bash: .setup.sh: command not found
Janes-MBP:basic-commits siyuhu$ cd git-katas
-bash: cd: git-katas: No such file or directory
Janes-MBP:basic-commits siyuhu$ cd basic-commit
-bash: cd: basic-commit: No such file or directory
Janes-MBP:basic-commits siyuhu$ git add README.md
Janes-MBP:basic-commits siyuhu$ git commit -m
error: switch `m' requires a value
usage: git commit [<options>] [--] <pathspec>...

    -q, --quiet           suppress summary after successful commit
    -v, --verbose         show diff in commit message template

Commit message options
    -F, --file <file>     read message from file
    --author <author>     override author for commit
    --date <date>         override date for commit
    -m, --message <message>
                          commit message
    -c, --reedit-message <commit>
                          reuse and edit message from specified commit
    -C, --reuse-message <commit>
                          reuse message from specified commit
    --fixup <commit>      use autosquash formatted message to fixup specified commit
    --squash <commit>     use autosquash formatted message to squash specified commit
    --reset-author        the commit is authored by me now (used with -C/-c/--amend)
    -s, --signoff         add Signed-off-by:
    -t, --template <file>
                          use specified template file
    -e, --edit            force edit of commit
    --cleanup <default>   how to strip spaces and #comments from message
    --status              include status in commit message template
    -S, --gpg-sign[=<key-id>]
                          GPG sign commit

Commit contents options
    -a, --all             commit all changed files
    -i, --include         add specified files to index for commit
    --interactive         interactively add files
    -p, --patch           interactively add changes
    -o, --only            commit only specified files
    -n, --no-verify       bypass pre-commit and commit-msg hooks
    --dry-run             show what would be committed
    --short               show status concisely
    --branch              show branch information
    --porcelain           machine-readable output
    --long                show status in long format (default)
    -z, --null            terminate entries with NUL
    --amend               amend previous commit
    --no-post-rewrite     bypass post-rewrite hook
    -u, --untracked-files[=<mode>]
                          show untracked files, optional modes: all, normal, no. (Default: all)

Janes-MBP:basic-commits siyuhu$ git commit -m "My commit message"
On branch master
Your branch is ahead of 'origin/master' by 1 commit.
  (use "git push" to publish your local commits)

Untracked files:
	../3-way-merge/.Rhistory
	example.txt

nothing added to commit but untracked files present
Janes-MBP:basic-commits siyuhu$ git greeting
git: 'greeting' is not a git command. See 'git --help'.
Janes-MBP:basic-commits siyuhu$ touch example.txt to create a file
Janes-MBP:basic-commits siyuhu$ git status
On branch master
Your branch is ahead of 'origin/master' by 1 commit.
  (use "git push" to publish your local commits)

Untracked files:
  (use "git add <file>..." to include in what will be committed)

	../3-way-merge/.Rhistory
	a
	create
	example.txt
	file
	to

nothing added to commit but untracked files present (use "git add" to track)
Janes-MBP:basic-commits siyuhu$ echo content > example.txt
Janes-MBP:basic-commits siyuhu$ dfsfdff
-bash: dfsfdff: command not found
Janes-MBP:basic-commits siyuhu$ git log
commit 8ebb496b076bd1b899c00ed305ac860a65113139 (HEAD -> master, greeting)
Author: drinkspritee <siyuh4@uci.edu>
Date:   Fri Jan 24 19:18:14 2020 -0800

    Add greeting

commit f8712d5c4df74fa0d49c8cc9ba3b1a5b2c571072 (origin/master, origin/HEAD)
Author: Frank Theile <ftheile@grundfos.com>
Date:   Mon Dec 9 10:30:13 2019 +0100

    Add missing shebang in squashing/setup.sh
    
    `setup.sh` should be executable according to the instructions given in README.md

commit e060df632bf4799da9aa1c0092640563acf84588
Author: Adam Matan <adamatan@users.noreply.github.com>
Date:   Wed Dec 4 07:46:31 2019 +0200

    Word ordering

commit 6ccb85882dc12fb0b26acd65bead2fc7da57a187
Author: Frank Theile <ftheile@grundfos.com>

[2]+  Stopped                 git log
Janes-MBP:basic-commits siyuhu$ echo this is the example file > example.txt
Janes-MBP:basic-commits siyuhu$ get status
-bash: get: command not found
Janes-MBP:basic-commits siyuhu$ git status
On branch master
Your branch is ahead of 'origin/master' by 1 commit.
  (use "git push" to publish your local commits)

Untracked files:
  (use "git add <file>..." to include in what will be committed)

	../3-way-merge/.Rhistory
	a
	create
	example.txt
	file
	to

nothing added to commit but untracked files present (use "git add" to track)
Janes-MBP:basic-commits siyuhu$ git add 
Nothing specified, nothing added.
Maybe you wanted to say 'git add .'?
Janes-MBP:basic-commits siyuhu$ git log --oneline
8ebb496 (HEAD -> master, greeting) Add greeting
f8712d5 (origin/master, origin/HEAD) Add missing shebang in squashing/setup.sh
e060df6 Word ordering
6ccb858 Mention `less` in SHELL-BASICS.md
f805e2a Added kata for .gitattributes
9669044 Simplify `git lol` alias
892d64f Fix link in squashing-README
1f9ead1 Minor improvements to submodules/README.md
956ac8d Removed reference to 'git rev-pars'
9313b5a Improved squashing/README.md
eb6c517 Added kata about git tags.
451a2b0 Update README.md
5ccbc50 Changed "git" to "Git" in detached-head/README
f94e033 Added to the task detached-head/README.
1b921a4 Added The task in save-my-commit/README.md
c9df4ca Added to The task in reverted-merge/README.md
e52649c Added to The task in merge-conflict/README.md
ac8f6c2 Added The task to commit-on-wrong-branch/README.md
2e29b3b Added the task section to bad-commit/README.md
66f5b27 Added useful commands and more to reset/README
8100f96 Add clone step to README Gif
ee01d2c Added to the task in reorder-the-history/README.
f56e566 Added useful commands section to amend/README.

[3]+  Stopped                 git log --oneline
Janes-MBP:basic-commits siyuhu$ git commit -m "another commit message"
On branch master
Your branch is ahead of 'origin/master' by 1 commit.
  (use "git push" to publish your local commits)

Untracked files:
	../3-way-merge/.Rhistory
	a
	create
	example.txt
	file
	to

nothing added to commit but untracked files present
Janes-MBP:basic-commits siyuhu$ git push
Username for 'https://github.com': drinkspritee
Password for 'https://drinkspritee@github.com': 
remote: Permission to praqma-training/git-katas.git denied to drinkspritee.
fatal: unable to access 'https://github.com/praqma-training/git-katas.git/': The requested URL returned error: 403
Janes-MBP:basic-commits siyuhu$ git log
commit 8ebb496b076bd1b899c00ed305ac860a65113139 (HEAD -> master, greeting)
Author: drinkspritee <siyuh4@uci.edu>
Date:   Fri Jan 24 19:18:14 2020 -0800

    Add greeting

commit f8712d5c4df74fa0d49c8cc9ba3b1a5b2c571072 (origin/master, origin/HEAD)
Author: Frank Theile <ftheile@grundfos.com>
Date:   Mon Dec 9 10:30:13 2019 +0100

    Add missing shebang in squashing/setup.sh
    
    `setup.sh` should be executable according to the instructions given in README.md

commit e060df632bf4799da9aa1c0092640563acf84588
Author: Adam Matan <adamatan@users.noreply.github.com>
Date:   Wed Dec 4 07:46:31 2019 +0200

    Word ordering

commit 6ccb85882dc12fb0b26acd65bead2fc7da57a187
Author: Frank Theile <ftheile@grundfos.com>

[4]+  Stopped                 git log
Janes-MBP:basic-commits siyuhu$ get status
-bash: get: command not found
Janes-MBP:basic-commits siyuhu$ git status
On branch master
Your branch is ahead of 'origin/master' by 1 commit.
  (use "git push" to publish your local commits)

Untracked files:
  (use "git add <file>..." to include in what will be committed)

	../3-way-merge/.Rhistory
	a
	create
	example.txt
	file
	to

nothing added to commit but untracked files present (use "git add" to track)
Janes-MBP:basic-commits siyuhu$ git log
commit 8ebb496b076bd1b899c00ed305ac860a65113139 (HEAD -> master, greeting)
Author: drinkspritee <siyuh4@uci.edu>
Date:   Fri Jan 24 19:18:14 2020 -0800

    Add greeting

commit f8712d5c4df74fa0d49c8cc9ba3b1a5b2c571072 (origin/master, origin/HEAD)
Author: Frank Theile <ftheile@grundfos.com>
Date:   Mon Dec 9 10:30:13 2019 +0100

    Add missing shebang in squashing/setup.sh
    
    `setup.sh` should be executable according to the instructions given in README.md

commit e060df632bf4799da9aa1c0092640563acf84588
Author: Adam Matan <adamatan@users.noreply.github.com>
Date:   Wed Dec 4 07:46:31 2019 +0200

    Word ordering

commit 6ccb85882dc12fb0b26acd65bead2fc7da57a187
Author: Frank Theile <ftheile@grundfos.com>

[5]+  Stopped                 git log
Janes-MBP:basic-commits siyuhu$ 
