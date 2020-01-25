# 191--siyu-hu-
Last login: Fri Jan 24 19:08:40 on ttys001

The default interactive shell is now zsh.
To update your account to use zsh, please run `chsh -s /bin/zsh`.
For more details, please visit https://support.apple.com/kb/HT208050.
dhcp-v112-222:191 github siyuhu$ cd git-katas
dhcp-v112-222:git-katas siyuhu$ cd 3-way-merge
dhcp-v112-222:3-way-merge siyuhu$ git branch greeting
fatal: A branch named 'greeting' already exists.
dhcp-v112-222:3-way-merge siyuhu$ git checkout greeting
A	3-way-merge/greeting.txt
Already on 'greeting'
dhcp-v112-222:3-way-merge siyuhu$ git commit -m
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

dhcp-v112-222:3-way-merge siyuhu$ git commit -m "Add greeting"
[greeting 8ebb496] Add greeting
 1 file changed, 3 insertions(+)
 create mode 100644 3-way-merge/greeting.txt
dhcp-v112-222:3-way-merge siyuhu$ git checkout master
Switched to branch 'master'
Your branch is up to date with 'origin/master'.
dhcp-v112-222:3-way-merge siyuhu$ touch README.md
dhcp-v112-222:3-way-merge siyuhu$ add README.md
-bash: add: command not found
dhcp-v112-222:3-way-merge siyuhu$ git add README.md
dhcp-v112-222:3-way-merge siyuhu$ git commit -m "Add README.md"
On branch master
Your branch is up to date with 'origin/master'.

Untracked files:
	.Rhistory

nothing added to commit but untracked files present
dhcp-v112-222:3-way-merge siyuhu$ git log --oneline --graph --all
* 8ebb496 (greeting) Add greeting
* f8712d5 (HEAD -> master, origin/master, origin/HEAD) Add missing shebang in squashing/setup.sh
* e060df6 Word ordering
* 6ccb858 Mention `less` in SHELL-BASICS.md
* f805e2a Added kata for .gitattributes
* 8ebb496 (greeting) Add greeting
* f8712d5 (HEAD -> master, origin/master, origin/HEAD) Add missing shebang in sq
uashing/setup.sh
* e060df6 Word ordering
* 6ccb858 Mention `less` in SHELL-BASICS.md
* f805e2a Added kata for .gitattributes
* 9669044 Simplify `git lol` alias
* 892d64f Fix link in squashing-README
| * c13fcff (origin/Expand_on_submodule_kata) Fix three typos
| * d9711cd Expand  on  submodules kata
|/  
* 1f9ead1 Minor improvements to submodules/README.md
* 956ac8d Removed reference to 'git rev-pars'
* 9313b5a Improved squashing/README.md
* eb6c517 Added kata about git tags.
* 451a2b0 Update README.md
* 5ccbc50 Changed "git" to "Git" in detached-head/README
* f94e033 Added to the task detached-head/README.
* 1b921a4 Added The task in save-my-commit/README.md
* c9df4ca Added to The task in reverted-merge/README.md
* e52649c Added to The task in merge-conflict/README.md
* ac8f6c2 Added The task to commit-on-wrong-branch/README.md
* 2e29b3b Added the task section to bad-commit/README.md

[1]+  Stopped                 git log --oneline --graph --all
dhcp-v112-222:3-way-merge siyuhu$ git add README.md
dhcp-v112-222:3-way-merge siyuhu$ git git diff greeting.txt README.md
git: 'git' is not a git command. See 'git --help'.

The most similar command is
	init
dhcp-v112-222:3-way-merge siyuhu$ git diff greeting.txt README.md
fatal: ambiguous argument 'greeting.txt': unknown revision or path not in the working tree.
Use '--' to separate paths from revisions, like this:
'git <command> [<revision>...] -- [<file>...]'
dhcp-v112-222:3-way-merge siyuhu$ git merge greeting.txt README.md
merge: greeting.txt - not something we can merge
dhcp-v112-222:3-way-merge siyuhu$ git merge greeting 
Updating f8712d5..8ebb496
Fast-forward
 3-way-merge/greeting.txt | 3 +++
 1 file changed, 3 insertions(+)
 create mode 100644 3-way-merge/greeting.txt
dhcp-v112-222:3-way-merge siyuhu$ git diff greeting master
dhcp-v112-222:3-way-merge siyuhu$ git merge greeting mater
merge: mater - not something we can merge
dhcp-v112-222:3-way-merge siyuhu$ git merge greeting master
Already up to date.
dhcp-v112-222:3-way-merge siyuhu$ 
