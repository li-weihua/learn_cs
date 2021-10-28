git tricks
==========

How to delete all commit history in github?
-------------------------------------------
::

    git checkout --orphan latest_branch
    git add -A
    git commit -am "commit message"
    git branch -D master
    git branch -m master
    git push -f origin master

How to rewrite previous commit usernames and emails
----------------------------------------------------
reference: https://stackoverflow.com/questions/2919878/git-rewrite-previous-commit-usernames-and-emails

::

    git config --global alias.change-commits '!'"f() { VAR=\$1; OLD=\$2; NEW=\$3; shift 3; git filter-branch --env-filter \"if [[ \\\"\$\`echo \$VAR\`\\\" = '\$OLD' ]]; then export \$VAR='\$NEW'; fi\" \$@; }; f"
    git change-commits GIT_AUTHOR_NAME "old name" "new name"
    git change-commits GIT_AUTHOR_EMAIL "old@email.com" "new@email.com"


change last commit ::

    git commit --amend --author="Author Name <email@address.com>" --no-edit
