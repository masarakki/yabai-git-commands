# yabai-git-commands

## setup

    $ git clone https://github.com/masarakki/yabai-git-commands
    $ export PATH=/path/to/yabai-git-commands/bin:$PATH

## commands

### git start

    $ git start new-branch

- create `new-branch` branch
- commit with 'new-branch' message

### git save

    $ git save [options]

- commit with 'fixup! branch-name'
- options pass to git commit command.
  for example, It can use commit all modified files.
  ex) "git save -a" is expand to "git commit -a -m 'fixup! branch-name'"

### git squash

    $ git squash

- squash fixup! commits

## workflow

    $ hub fork
    $ git start new-branch
    # edit something
    $ git add .
    $ git save
    # edit something
    $ git add .
    $ git save
    $ git squash
    $ git push myfork new-branch
    $ hub pull-request

You must think **branch name** only.
